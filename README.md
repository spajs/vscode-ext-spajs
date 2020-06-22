# SPAjs

## HTML & Javascript Code Snippets for [SPA.js](https://spa.js.org)

![Overview](https://media.giphy.com/media/3ohs4fuOhWNBI991Ha/giphy.gif)

---
## In **[.html]** file:

> ### HTML boilerplates
| Shortcut            | Code
|-                    |-
| !html-spa           | HTML boilerplate with SPA + dependency cdn links
| !html-spa+bootstrap | HTML boilerplate with SPA + dependency + Bootstrap cdn links
| !template-component | SPA Component boilerplate
| -container          | SPA Component boilerplate
| !!                  | minimal HTML5 boilerplate

> ### CDN Links with corresponding tag and attribute
| Shortcut           | Code                                                                        | Home
|-                   |-                                                                            |-
| cdn:boot-css       | //cdn.jsdelivr.net/npm/bootstrap@{4.5.0}/dist/css/bootstrap.min.css         | [Bootstrap](https://getbootstrap.com/)
| cdn:boot-js        | //cdn.jsdelivr.net/npm/jquery@{latest}/dist/jquery.min.js<br>//cdn.jsdelivr.net/npm/popper.js@{latest}/dist/umd/popper.min.js<br>//cdn.jsdelivr.net/npm/bootstrap@{4.5.0}/dist/js/bootstrap.min.js                          | [Bootstrap](https://getbootstrap.com/)
| cdn:spa            | //cdn.jsdelivr.net/npm/jquery@latest/dist/jquery.min.js<br>//cdn.jsdelivr.net/npm/handlebars@latest/dist/handlebars.min.js<br>//cdn.jsdelivr.net/gh/sucom/SPA.js/dist/spa-bundle.min.js                           | [SPA.js](https://spa.js.org)
| cdn:jq             | //cdn.jsdelivr.net/npm/jquery@{latest}/dist/jquery.min.js                   | [jQuery](https://jquery.com/)
| cdn:jq-slim        | //cdn.jsdelivr.net/npm/jquery@{latest}/dist/jquery.slim.min.js              | [jQuery](https://jquery.com/)
| cdn:handlebars     | //cdn.jsdelivr.net/npm/handlebars@{latest}/dist/handlebars.min.js           | [Handlebars](https://handlebarsjs.com/)
| cdn:lodash         | //cdn.jsdelivr.net/npm/lodash@{latest}/lodash.min.js                        | [Lodash](https://lodash.com/)
| cdn:altiframe-es5  | //cdn.jsdelivr.net/gh/FrontEndNeo/alt-iframe/dist/es5/alt-iframe.min.js     | [alt-iframe](https://github.com/FrontEndNeo/alt-iframe)
| cdn:altiframe-es6  | //cdn.jsdelivr.net/gh/FrontEndNeo/alt-iframe/dist/es6/alt-iframe.min.js     | [alt-iframe](https://github.com/FrontEndNeo/alt-iframe)

> ### meta tags
| Shortcut           | Code
|-                   |-
| meta:seo           | SEO meta tags
| meta:cache         | no-cache meta tags

> ### tags
| Shortcut           | Code
|-                   |-
| fav:icon           | fav-icon link to image
| fav:base64         | fav-icon link with [href=base64]
| spa$               | \<spa-component src="{componentName}">\</spa-component>
| spa-component      | \<spa-component src="{componentName}">\</spa-component>
| -component         | \<x-component src="{componentName}">\</x-component>
| x-component        | \<x-component src="{componentName}">\</x-component>
| template           | \<template id="{template-id}">\</template>
| -template          | \<x-template src="{componentName}">\</x-template>
| x-template         | \<x-template src="{componentName}">\</x-template>
| spa-template       | \<spa-template src="{componentName}">\</spa-template>


> ### spa-component-attribute [ data-x-component="{componentName}" ]
| Shortcut
|-
| :component
| :spa-component
| :data-spa-component
| :data-x-component

> ### spa-attributes (i18n)
| Shortcut            | Attribute                                 | tag / purpose
|-                    |-                                          |-
| i18n-lang           | i18n-lang="{en_US}"                       | \<body>; for default i18n lang
| i18n-lang-switch    | data-i18n-lang="{en_US}"                  | \<a> or \<button>; for i18n lang switch
| :i18n               | data-i18n="{i18n.key}"                    | \<any>; for i18n.key text inside the tag

> ### spa-attributes (route)
| Shortcut            | Attribute                                 | tag / purpose
|-                    |-                                          |-
| :route              | data-spa-route="{route/path}"             | \<a> or \<button>; for route
| :route-params       | data-spa-route-params="{param}:'{value}'" | \<a> or \<button>; for route param
| :show-nav           | class="SHOW-SPA-NAV"                      | \<body>; to show routes in address bar
| :hide-nav           | class="HIDE-SPA-NAV"                      | \<body>; to hide routes in address bar

> ### \<a> attributes
| Shortcut            | Attribute
|-                    |-
| a:rel               | rel="noopener noreferrer"
| a:target            | target="_blank" rel="noopener noreferrer"
| target:blank        | target="_blank" rel="noopener noreferrer"

> ### [for] attribute (experimental)
| Shortcut            | Attribute                             | tag / purpose
|-                    |-                                      |-
| :for                | for="componentName"                   | \<a> or \<button>; to render component on click of this element

> ### Handlebars template - custom helpers
| Shortcut              | Attribute                             | tag / purpose
|-                      |-                                      |-
| :$()                  | {${componentName}}{method}();         | \<any onevent="...">; to call component method in [onevent]
| :consoleClear         | {{:consoleClear }}
| :consoleLog           | {{:consoleLog {variable} }}
| :trim                 | {{:trim {srcStringVariable} }}
| :trimStr              | {{:trimStr {srcStringVariable} '{trimString}' }}
| :trimLeft             | {{:trimLeft {srcStringVariable} }}
| :trimLeftStr          | {{:trimLeftStr {srcStringVariable} '{trimString}' }}
| :trimRight            | {{:trimRight {srcStringVariable} }}
| :trimRightStr         | {{:trimRightStr {srcStringVariable} '{trimString}' }}
| :replaceStr           | {{:replace {srcStringVariable} searchStr='{searchForString}' replaceStr='{replaceWithString}' }}
| :replaceStringOnRegEx | {{:replace {srcStringVariable} rxPattern='{searchForRegExPattern}' rxOption='{g,i,gi}' replaceStr='{replaceWithString}' }}
| :getLeftStrByIndex    | {{:getLeftStr {srcStringVariable} {fromIndexNumber} }}
| :getLeftStrByString   | {{:getLeftStr {srcStringVariable} '{fromSplitString}' }}
| :getRightStrByIndex   | {{:getRightStr {srcStringVariable} {fromIndexNumber} }}
| :getRightStrByString  | {{:getRightStr {srcStringVariable} '{fromSplitString}' }}
| :normalizeStr         | {{:normalize {srcStringVariable} }}
| :toLowerCase          | {{:toLowerCase {srcStringVariable} }}
| :toUpperCase          | {{:toUpperCase {srcStringVariable} }}
| :toTitleCase          | {{:toTitleCase {srcStringVariable} }}
| :capitalize           | {{:capitalize {srcStringVariable} }}
| :unCapitalize         | {{:unCapitalize {srcStringVariable} }}
| :toString             | {{:toStr {srcObjectVariable} }}
| :toBoolean            | {{:toBool {srcStringVariable} }}
| :dateNowMs            | {{:dateNowMs }}
| :dateNow              | {{:dateNow '{formatString}' }}
| :dateNowFormatHelp    | {{:dateNowFormatHelp }}
| :moment               | {{:moment {srcDateTimeStringVariable} '{srcFormatString}' '{targetFormatString}' }}
| :rand                 | {{:rand {minNumber} {maxNumber} }}
| :randPwd              | {{:randPwd {passwordLength} '{passwordCharacters}' }}


---

## In **[componentX.js]** file:

> ### Generic
| Shortcut     | code
|-             |-
| f            | Anonymous function
| fn           | Named function
| clg or clog  | console.log()

> ### spa component
| Shortcut        | output
|-                |-
| nsc or newSpa$  | SPA Component new template (SPA v2.84.0+)
| spa$ or spa.$   | SPA Component base properties (old template for prior SPA v2.84.0)
| spa$extend      | SPA Component extended properties (old template for prior SPA v2.83.0)

> ### spa component properties
| Shortcut        | output
|-                |-
| $_              | define base properties (new SPA v2.84.0+)
| $.              | define base properties inside spa.$( 'componentX', { ... } ) prior to SPA v2.83.0

> ### spa component path/name
| Shortcut        | output
|-                |-
| spa$#           | component name
| spa$/           | component path
| spa$filename    | component file name
| //#sourceURL    | sourceURL for debugging

> ### access spa component properties / methods
| Shortcut        | output
|-                |-
| app$            | current component method
| app$$           | other component method

> ### call spa component methods
| Shortcut        | output
|-                |-
| spa$render      | render component
| spa$refresh     | refresh component
| spa$show        | show component
| spa$hide        | hide component
| spa$enable      | enable clicks
| spa$disable     | disable clicks
| spa$remove      | remove component
| spa$destroy     | destroy component

> ### spa.utils
| Shortcut ( spa. )
|-
| .bindData
| .bindTemplateData
| .dataBind
| .defaults
| .doDataValidation
| .validateForm
| .findInObj
| .getElValue
| .getLocHash
| .getModifiedElements
| .hasKey
| .hasKeyIgnoreCase
| .hasKeys
| .hasPrimaryKeys
| .i18n.text
| .i18n.apply
| .i18n.updateLang
| .is
| .isBlank
| .isElementExist
| .isElValueChanged
| .now
| .onUrlHashChange
| .queryStringToObject
| .rand
| .randomPassword
| .range
| .resetElementsDefaultValue
| .serializeFormToSimpleObject
| .serializeFormToObject
| .toQueryString
| .year
| .urlHash


> ### String utils
| Shortcut
|-
| .beginsWithStr
| .beginsWithStrIgnoreCase
| .endsWithStr
| .endsWithStrIgnoreCase
| .containsStr
| .containsStrIgnoreCase
| .equalsIgnoreCase
| .extractStrBetweenIn
| .extractStrBetweenEx
| .getLeftStrByIndex
| .getLeftStrByStr
| .getRightStrByIndex
| .getRightStrByStr
| .isBlankStr
| .ifBlankStr
| .isNumberStr
| .trimStr
| .trimLeftStr
| .trimRightStr
| .normalizeStr
| .capitalize
| .unCapitalize
| .toProperCase
| .toJSON
| .toNative
| .splitToArray


> ### Object utils
| Shortcut
|-
| .__clone
| .__merge
| .__stringify
| .__toQueryString
| .__keys
| .__keysAll
| .__hasKey
| .__hasKeysAll
| .__hasKeysAny
| .__hasPrimaryKeysAll
| .__hasPrimaryKeysAny
| .__valueOf

---
## For more information on SPA.js

- [SPA.js - Home](https://spa.js.org)
- [spa-cli - npm command line interface](https://www.npmjs.com/package/spa-cli)

---
