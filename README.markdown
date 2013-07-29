jQuery package
==============

quickly include jQuery on Visualforce pages.

 * quick start
 * documentation
 * more info

quick start
-----------

install the managed package by following these links:

 * [Production install](https://login.salesforce.com/packaging/installPackage.apexp?p0=04ti000000019SU)
 * [Sandbox install](https://test.salesforce.com/packaging/installPackage.apexp?p0=04ti000000019SU)

add one of the components to your pages and you're off.

```visualforce
<jQuery:Core />
```

```visualforce
<jQuery:UI />
```

```visualforce
<jQuery:Mobile />
```

documentation
-------------

loads the latest versions of jQuery (currently 1.9.1),
jQuery UI (currently 1.10.3) and/or jQuery Mobile
(currently 1.3.0), then automatically calls
`jQuery.noConflict()` to avoid collision with the other
libraries loaded by Salesforce, so use `jQuery` and not `$`,
or wrap your code in a closure.

```visualforce
<apex:page>
    <jQuery:UI theme="le-frog" min="false" onReady="init();" />
    <script>
        function init() {

            // doSomeStuff

        }
    </script>
</apex:page>
```

attributes:
 * `alias`: alias to use for global jQuery variable
 * `min`: whether to include the minified source files
 * `onReady`: JavaScript code to execute when the DOM is loaded
 * `theme`: the theme to include (only for UI: see [Themeroller](http://jqueryui.com/themeroller/))
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
 * <http://www.jquerymobile.com>
