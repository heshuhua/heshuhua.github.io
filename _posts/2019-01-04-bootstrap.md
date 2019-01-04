---
layout: post
title:  bootstrap
date:   2019-01-04 09:00:00 +0800
categories: engineering
---
bootstrap 的一些用法
### 命名的缩写。
https://getbootstrap.com/docs/4.0/utilities/spacing/
采用的格式 The classes are named using the format {property}{sides}-{size} for xs and {property}{sides}-{breakpoint}-{size} for sm, md, lg, and xl.

m代表margin，p代表padding

例如：
.mt-0 {
  margin-top: 0 !important;
}

.ml-1 {
  margin-left: ($spacer * .25) !important;
}
