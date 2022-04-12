---
layout: post
title: RSS tricks & hooks in WordPress
description: Compilation of rss hooks for CMS WordPress
---

# RSS tricks & hooks in CMS WordPress

```
/* add thumbnails to RSS feed in Wordpress - edit functions.php */
 
add_filter( 'the_excerpt_rss', 'add_thumbnail_to_feed' );
add_filter( 'the_content_feed', 'add_thumbnail_to_feed' );
 
function add_thumbnail_to_feed( $content ){
    $img = get_the_post_thumbnail( null, array(100, 80), array( 'align' => 'left', 'style' => 'margin-right:15px;' ) );
    $content =  $img . $content;
 
    return $content;
}
 
/* make delay for the sending posts to RSS in WordPress */
 
function publish_later_on_feed($where) {
global $wpdb;if ( is_feed() ) {
$now = gmdate('Y-m-d H:i:s');
$wait = '5'; // your delay
$device = 'MINUTE'; // you can change to MINUTE, HOUR, DAY, WEEK, MONTH, YEAR
$where .= " AND TIMESTAMPDIFF($device, $wpdb->posts.post_date_gmt, '$now') > $wait ";
}
return $where;
}
add_filter('posts_where', 'publish_later_on_feed');
 
/* exclude category from homepage and RSS feed in WordPress */
 
function exclude_category($query) {
 if ($query->is_feed || ($query->is_home || ($query->is_search))){
 $query->set('cat','-YOUR_CATEGORY_ID');} 
 return $query; }
add_filter('pre_get_posts','exclude_category');
 
// if you want exclude only from RSS-feed:
 
function myFilter($query) {
if ($query->is_feed) {
$query->set('cat','-YOUR_CATEGORY_ID');
}
return $query;
}
 
add_filter('pre_get_posts','myFilter');
```
[back]({{ site.url }})