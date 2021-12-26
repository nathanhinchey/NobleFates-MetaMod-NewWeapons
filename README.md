# MetaMod: New Weapons
this is an app for generating octdats, the format used for data in
[Noble Fates](https://noblefates.com/). THIS IS NOT A MOD. I'm calling this a
meta-mod, because it's a tool for making mods.

As of right now (2021-12-26) it doesn't do anything.

## Templates: `*.octdat.template`
These are files that are similar in format to OctDats, except key values have
been replaced with `<% foo %>` where `foo` is a variable that will be
substituted in. For example, if the template says

```
    minQuality = <% gripMinQuality %>
    chanceFrom = <% gripChanceFrom %>
    chanceTo = <% gripChanceTo %>
```

and we compile the template with the value for `gripMinQuality` set to `.1`,
`gripChanceFrom` set to `.5` and `gripChanceTo` set to `1`, then the output
file would instead have this:

```
minQuality = .1
chanceFrom = .5
chanceTo = 1
```

## URLS
So, this is a bit ambitious, but I plan to have everything saved in the query
string, so that if someone sends you a link to their custom weapon, you can
modify it as you see fit. For example, if the page was hosted at
`example.com/example.html`, then for the above example you would have the
URL
`example.com/example.html?gripMinQuality=4&gripChanceFrom=.5&gripChanceTo=1`.
