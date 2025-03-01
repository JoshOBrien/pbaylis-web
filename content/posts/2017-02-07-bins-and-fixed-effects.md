---
layout: post
title:  "Bins and fixed effects"
date:   2017-02-07
categories: 
  - econometrics
tags:
  - r
  - bins
---

We often estimate dose-response functions of outcome Y on temperature by combining binned regression with fixed effects. It can be important to consider the functional form chosen here and what it implies for extrapolation.

- OLS can be strongly influenced by outliers. In fixed effects models with bins, outliers can be less obvious: unusually hot or cold day for a given region in a given season, for example. This means that errors in either the outcome or the RHS become more important, as do infrequently observed days.
- Still, the edges of the response function are determined (in splined or binned models) primarily by regions/seasons that typically experience that kind of weather. Extrapolation a problem for that reason as well.

Here's what other people say about these questions:
- [Auffhammer, Hsiang, Schlenker, Sobel 2014](https://oup.silverchair-cdn.com/oup/backfile/Content_public/Journal/reep/7/2/10.1093/reep/ret016/2/ret016.pdf?Expires=1486859944&Signature=b6zTIZvA6L3fGU9wRoaY7egm6N4QqKECqnxnQGWstQwE77P9RdS39qOxCSXM-cdrDDPtHKyChXx02D9oxSmVNNdJCw-HdQLmmKccJBMmx17ZQL9iwQuO0rb14V31~K~FbCYK2tkt-Ix8MyQtTaIyyuDs23o67ggD3O~fw6FaEazqzaVkavZ2rbNb4~fHPFscjAwoy3xxNQW8Nm-HCpe9fuQ2n-DrxTvZTM9ULzv0n6RmvFRCS1CH1tSYN7MMfp0~L0eLq3qU~8~f2eGVcq572cXfjLHYfFUacBcSQBmXRY7qZgmvSxyWnSluCE882wgVdKSUTa9UxdvBNG-e5CkVlA__&Key-Pair-Id=APKAIUCZBIA4LVPAVW3Q)
- [Hsiang 2016](http://www.nber.org/papers/w22181)
- [Dell, Jones, and Olken 2014](http://economics.mit.edu/files/9138)
