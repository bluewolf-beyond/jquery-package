jQuery package
==============

quickly include jQuery on Visualforce pages.

 * quick start
 * documentation
 * more info

quick start
-----------

install the managed package by following these links:

 * [Production install](https://login.salesforce.com/packaging/installPackage.apexp?p0=04ti000000018By)
 * [Sandbox install](https://test.salesforce.com/packaging/installPackage.apexp?p0=04ti000000018By)

add the component to your pages and you're off.

```visualforce
<apex:page>
    <jQuery:UI />
</apex:page>
```

documentation
-------------

loads the latest versions of jQuery (currently 1.9.1) and
jQuery UI (currently 1.10.2).  automatically calls
`jQuery.noConflict()` to avoid collision with the other
libraries loaded by Salesforce, so use `jQuery` and not `$`,
or wrap your code in a closure.

```visualforce
<apex:page>
    <jQuery:UI theme="le-frog" min="false" />
    <script>
        (function($) {
            $(function() {

                // doSomeStuff

            });
        })(jQuery);
    </script>
</apex:page>
```

attributes:
 * `min`: whether to include the minified source files
 * `theme`: the theme to include (see [Themeroller](http://jqueryui.com/themeroller/))
   * black-tie
   * blitzer
   * cupertino
   * dark-hive
   * dot-luv
   * eggplant
   * excite-bike
   * flick
   * hot-sneaks
   * humanity
   * le-frog
   * mint-choc
   * overcast
   * pepper-grinder
   * redmond
   * smoothness
   * south-street
   * start
   * sunny
   * swanky-purse
   * trontastic
   * ui-darkness
   * ui-lightness
   * vader

more info
---------

 * <http://www.jquery.com>
 * <http://www.jqueryui.com>
