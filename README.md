# jtwt.js - a simple jQuery plugin for the twitter Search API

jtwt.js is an easy-to-use jQuery plugin that allows you to display your recent tweets on your website or elsewhere.

## Usage

At first you will need to implement the jQuery library in the ```<head>``` area of your document, like this:

```
<script type="text/javascript" src="js/jquery.js"></script>
```

Add the jtwt.js and the jtwt.css below the jQuery library:

```
<script type="text/javascript" src="js/jtwt.min.js"></script>
<link rel="stylesheet" href="css/jtwt.css" />
```

Now initialize the jtwt plugin between a ```$(window).load(function() {``` and a ```});```.

```
<script type="text/javascript">
  $(window).load(function() {
		$('#twitter').jtwt({
			username : 'yourusername'
		});
	});
</script>
```

At last, we need to create the already declared container for our twitter widget:

```
<div id="twitter"></div>
```

## Options

jtwt.js comes with a bunch of options to create the best experience for your users.

```
$('#twitter').jtwt({
	count : int, // The number of displayed tweets.
	username : 'yourusername', // Your username.
	query : 'searchquery', // Performs a search query.
	convert_links : boolean, //Converts hashtags to links
	image_size : int, // The size of your avatar.
	loader_text : 'loading tweets', // loading text
	no_result : 'No tweets found' // no results text
});
```

Since jtwt.js makes use of Twitter's Search API, you can also perform search queries instead of displaying a users recent tweets.

To make use of this function, just assign the query option with suitable search query. There is no need for a username, you just need a query. If there is any username assigned, jtwt will just overwrite it with the given query.

```
$('#twitter').jtwt({
	query : '#batman', //Tweets with the hashtag #batman
});
```

jtwt can perform any search query that is valid to the syntax of Twitter's search function. For more information please visit: [https://dev.twitter.com/docs/using-search](https://dev.twitter.com/docs/using-search)

## Changelog

+ 10/26/2012 - Added retweet support + Bug fix
+ 1/15/2013 - Bug Fix + new time ago function (thanks to [@mikloshenrich](http://twitter.com/mikloshenrich))
+ 4/5/2013 - Changed to Twitter's search API + search query function

## License

jtwt.js is contributed under the [Creative Commons Attribution 3.0 Unported license](http://creativecommons.org/licenses/by/3.0/). You're free to use jtwt.js in personal and commercial projects.

## Support

jtwt.js is provided "as-is", without any warranty and professional support. However, we're happy to help if we can. [Feel to drop us a line](mailto:support@hrbor.com). It may take up to 48 hours till you receive an answer.
