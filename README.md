jQuery ScrollPaging
========

Pagination with scroll.
Copyright (c) 2013 Artod - gartod@gmail.com

Demo
----------

http://artod.ru/jquery-scroll-paging/demo/

How to use
----------

To get started, download the plugin, unzip it and copy files to your website/application directory.
Load files in the 'head' section of your HTML document. Make sure you also add the jQuery library.

    <head>
        <script src="http://ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>		
        <script src="jquery.scroll-paging.js"></script>
    </head>

Initialise the script like this:

    <script>
        $(document).ready(function() {
			$.scrollPaging({
				$viewport: $(window),
				$scrollable: $(document),
				additive: 100,
				getPage: function(scrollPaging) {
					scrollPaging.opts.$scrollable.append('Page #' + scrollPaging.page + '<br />');
					scrollPaging.page++;
				}
			});
        });
    </script>