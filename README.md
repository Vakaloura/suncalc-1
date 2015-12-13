
# suncalc

<!-- This file was generated by scripts/template. Do not edit this file directly but
     instead have a look at: metainfo.json, templates/README.md.j2. -->

[![Build Status](https://travis-ci.org/ypid/suncalc.svg?branch=master)](https://travis-ci.org/ypid/suncalc)
[![haxelib version](https://img.shields.io/badge/Haxe-v1.7.0-blue.svg)](http://lib.haxe.org/p/suncalc)
[![NPM version](https://img.shields.io/npm/v/suncalc.svg)](https://www.npmjs.org/package/suncalc)
[![Packagist version](https://img.shields.io/packagist/v/ypid/suncalc.svg)](https://packagist.org/packages/ypid/suncalc)


The SunCalc module allows to calculate sun position,
sunlight phases (times for sunrise, sunset, dusk, etc.),
moon position and lunar phase for the given location and time.

The library was ported to Haxe by [Robin `ypid` Schneider](https://github.com/ypid) to allow using it in a library for [opening hours](https://github.com/opening-hours/opening_hours.js/issues/136).

It is based on the [JavaScript implementation](https://github.com/mourner/suncalc)
created by [Vladimir Agafonkin](http://agafonkin.com/en) ([@mourner](https://github.com/mourner))
as a part of the [SunCalc.net project](http://suncalc.net).

Most calculations are based on the formulas given in the excellent Astronomy Answers articles
about [position of the sun](http://aa.quae.nl/en/reken/zonpositie.html)
and [the planets](http://aa.quae.nl/en/reken/hemelpositie.html).
You can read about different twilight phases calculated by SunCalc
in the [Twilight article on Wikipedia](https://en.wikipedia.org/wiki/Twilight).

Refer to the [API documentation](https://ypid.github.io/suncalc/suncalc/SunCalc.html) for details.

## Install

Install the library for your favorite language by executing one of the following commands:

```Shell
haxelib install suncalc         # Haxe
npm install suncalc             # JavaScript/Node.JS
composer require ypid/suncalc   # PHP
```

## Supported languages/platforms

* C++
* [Haxe](http://lib.haxe.org/p/suncalc) ([native port repository](https://github.com/mourner/suncalc))
* Java ([native port repository](https://github.com/mncaudill/SunCalc-Java))
* [JavaScript/Node.JS](https://www.npmjs.org/package/suncalc) ([native port repository](https://github.com/mourner/suncalc))
* NekoVM
* [PHP](https://packagist.org/packages/ypid/suncalc) ([target build repository](https://github.com/ypid/suncalc-php))
* Python ([native port repository](https://github.com/Broham/suncalcPy))

## Supported languages/platforms not generated by Haxe

* Go ([native port repository](https://github.com/mourner/suncalc-go))
* Objective-C ([native port repository](https://github.com/swerdlow/suncalc-objective-c))
* Swift ([native port repository](https://github.com/shanus/suncalc-swift))

## Limitations

The following limitations seems to be related which should mean that when they are fixed for one target, the tests for the other targets should also pass. If you need `SunCalc.getMoonTimes` for one of those targets, feel free to debug it further.

* Python: `SunCalc.getMoonTimes` (`rise` date can not be calculated.).
* C++: `SunCalc.getMoonTimes` (`segmentation fault`).
* Java: `SunCalc.getMoonTimes` (`java.lang.NullPointerException`).
* Neko: `SunCalc.getMoonTimes`

## Unsure/untested

* ActionScript 3: Does compile but I have no idea how to test it.
* Flash: Does compile but I have no idea how to test it.

## Unsupported

* C#: Dependency `datetime` does not compile on target "datetime/3,0,2/src/datetime/DateTime.hx:146: characters 28-110 : haxe.Int64 should be Float"

  Priority low.

## License

[BSD-2-Clause](https://tldrlegal.com/license/bsd-2-clause-license-%28freebsd%29)
