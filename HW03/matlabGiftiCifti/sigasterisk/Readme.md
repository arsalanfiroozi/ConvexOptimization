# Sigasterisk
> Implementing how significant two bars at a grouped bar plot is by adding '*' with [the shown](#screenshots) style.

## Table of contents
* [General info](#general-info)
* [Screenshots](#screenshots)
* [Setup](#setup)
* [Code Examples](#Code Examples)
* [Features](#features)
* [Contact](#contact)

## General info
These functions were created mainly because of:
1. Not supporting Matlab functions for asterisks to show how significant two bars are
2. Not supporting Matlab functions for adding errors to grouped bar plots
3. Not supporting similar shared functions adding asterisks for different bars in different groups 

## Screenshots
![Example screenshot](demo.png)

## Setup
Describe how to install / setup your local environement / add link to demo version.

## Code Examples

%% Fig1
figure;
set(gcf,'Color',[1 1 1]);
Data = transpose([45 33 18 37 42 30]);
ylim([0 50]);
bar(Data);
sigasterisk(1,1,2,5,"*",Data);
title("Fig 1");
export_fig("Fig1.png",'-r600');

%% Fig2
figure;
set(gcf,'Color',[1 1 1]);
Data = [10 20 30;15 20 5;45 90 10;16 17 13;80 10 30;40 60 10];
bar(Data);
sigasterisk(1,1,2,3,"*",Data);
sigasterisk(1,1,2,4,"*",Data);
title("Fig 2");
ylim([0 95]);
export_fig("Fig2.png",'-r600');

%% Fig3
figure;
set(gcf,'Color',[1 1 1]);
bar(Data);
sigasterisk(2,3,3,3,"*",Data);
title("Fig 3");
export_fig("Fig3.png",'-r600');

%% Fig4
figure;
set(gcf,'Color',[1 1 1]);
Errors = rand(6,3)*5;
bar(Data);
add_errorbar(Errors, Data);
sigasterisk(2,3,1,1,"*",Data,Errors);
title("Fig 4");
export_fig("Fig4.png",'-r600');


## Features
* You can change all dimensions which is used to plot by optional arguments

To-do list:
* Different height used if the function for a column is used twice.

## Contact
Created by [@arsalan.firoozi](https://ee.sharif.ir/~firoozi.arsalan) - feel free to contact me!