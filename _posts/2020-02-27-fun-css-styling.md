---
title: Fun CSS Styling
layout: post
tags: CSS
category: CSS
date: 2020-02-27T14:25:58.983Z
summary: CSS
excerpt_separator: ''
---
```
a {

  // font-size: smaller;
  // display: inline-block;
  // text-decoration: none;

  // text-decoration: none;
  text-shadow: 
     0px -2px 0 $sidebar-color,  0px -1px 0 $sidebar-color,  0px 0px 0 $sidebar-color,
     2px -2px 0 $sidebar-color,  2px -1px 0 $sidebar-color,  2px 0px 0 $sidebar-color,
    -2px -2px 0 $sidebar-color, -2px -1px 0 $sidebar-color, -2px 0px 0 $sidebar-color,
     1px -2px 0 $sidebar-color,  1px -1px 0 $sidebar-color,  1px 0px 0 $sidebar-color,
    -1px -2px 0 $sidebar-color, -1px -1px 0 $sidebar-color, -1px 0px 0 $sidebar-color,
     0px -2px 0 $sidebar-color,  0px -1px 0 $sidebar-color,  0px 0px 0 $sidebar-color;
  box-shadow: 
    0 -3px 0 0 $sidebar-color inset, 
    0 -3px 0 0 transparent inset;  
    
  transition: all .3s ease-in;
  
  &:hover {
    transition: all .3s ease-out;
    box-shadow:  0 -6px 0 0 $sidebar-color inset, 0 -8px 0 0 $title-color inset ;
  }

  // &::selection {
  //   color: $sidebar-color; background: $title-color;
  //   text-shadow: none;
  // } 
}

Cover from underline upwards 
a.underline-magical {
  background-image: linear-gradient(120deg, #84fab0 0%, #8fd3f4 100%);
  background-repeat: no-repeat;
  background-size: 100% 0.2em;
  background-position: 0 88%;
  transition: background-size 0.25s ease-in;
  &:hover {
    background-size: 100% 88%;
  }
}

Underline to right
a.left {
  position: relative;
}

a.left:before {
  content: "";
  position: absolute;
  width: 0;
  height: 2px;
  bottom: 0;
  left: 0;
  background-color: #FFF;
  visibility: hidden;
  transition: all 0.3s ease-in-out;
}

a.left:hover:before {
  visibility: visible;
  width: 100%;
}
```
