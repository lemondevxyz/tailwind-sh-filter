# tailwind-sh-filter
tailwind-sh-filter is a shell script to filter out unused CSS, tailored for tailwind css

## usage
```shell
cat data/page1.html data/page2.html data/page3.html | ./tailwind-sh-filter data/style1.css data/style2.css
```

## caveats
this script is rather conservative, and will not include and rulesets like:
```css
/* this ruleset will be excluded */
.matched-class, .unmatched-class { color: blue; }
```
```html
<div class="matched-class"></div>
```

there are other caveats, but I can't think of any atm.