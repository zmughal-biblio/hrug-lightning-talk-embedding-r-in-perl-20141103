# Embedding R in Perl

Houston R Users Group
2014 Nov 3rd

Zaki Mughal
Computational Biomedicine Lab, UH

<http://github.com/zmughal>


## R Extensions API
- Faster native code
- Writing R Extensions <http://cran.r-project.org/doc/manuals/r-release/R-exts.html>
- Inline R package for C and C++
- Rcpp
- Advanced R book <http://adv-r.had.co.nz/>

## Goals
- Run R functions

      R::library( ‘class’ );
      my ($test, $train, $class) = ( … ); # build data
      my $knn = R::knn( $train, $test, $class ); # factor

- Convert Perl data to R data and vice versa
  n-d arrays (PDL), data frames, factor variables

      my $knn_p = R::Convert::r_to_perl( $knn );

- RSPerl: conversion not dynamic

## Goals (II)
- Use R’s machine learning packages (for research)
- Have some fun with R, Perl, and C :-)
- Write a paper for J Stat Soft :-D

## R internals
- SEXP
  + INTSEXP
  + REALSEXP
  + CHARSEXP
  + CLOSEXP

## What works
- <https://github.com/zmughal/embedding-r-in-perl-experiment>
- <https://github.com/zmughal/data-frame-experiment>

## Future
- Finish the function calls
- Fix some rough edges with 1-based indices
- Write that paper!


vim: ft=markdown
