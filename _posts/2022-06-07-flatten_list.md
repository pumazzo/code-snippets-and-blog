---
layout: post
title: "A code snippet"
date: 2022-06-07
categories: code python 
excerpt_separator: <!--more-->
---

# How to flatten a list in pyton

How to flatten a list of list in python?

<!--more-->
'''
  def flatten(l, ltypes=(list, tuple)):
      ltype = type(l)
      l = list(l)
      i = 0
      while i < len(l):
          while isinstance(l[i], ltypes):
              if not l[i]:
                  l.pop(i)
                  i -= 1
                  break
              else:
                  l[i:i + 1] = l[i]
          i += 1
      return ltype(l)

  a = []
  for i in xrange(2000):
    a = [a, i]
  a = flatten(a)
 '''python
[sources](http://rightfootin.blogspot.com/2006/09/more-on-python-flatten.html)
