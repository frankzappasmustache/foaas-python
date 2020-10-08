foaas-python
============

A simple Python library to [FOAAS].

[![build status](https://secure.travis-ci.org/dmpayton/foaas-python.png)](http://travis-ci.org/dmpayton/foaas-python)
[![test coverage](https://coveralls.io/repos/dmpayton/foaas-python/badge.png)](https://coveralls.io/r/dmpayton/foaas-python)
[![downloads](https://pypip.in/d/foaas/badge.png)](https://crate.io/packages/foaas/)

* **Author**: [Derek Payton]
* **Version**: 0.2.0
* **License**: [MIT]

Documentation
-------------

### Installation

This package relies on [requests] and should be installed with [pip]:

```
pip install foaas
```

### Basic Usage

Fuck off:

```
>>> from foaas import fuck
>>> print fuck.off(name='Tom', from_='Chris').text
Fuck off, Tom. - Chris
```

Give me some fucking JSON:

```
>>> fuck.that(from_='Chris').json
{u'message': u'Fuck that.', u'subtitle': u'- Chris'}
```

Just get the fucking URL:

```
>>> print fuck.everything(from_='Chris').url
http://foaas.herokuapp.com/everything/Chris
```

This needs to be fucking secure:

```
>>> from foaas import Fuck
>>> fuck = Fuck(secure=True)
>>> fucking = fuck.life(from_='Phil')
>>> print fucking.url
https://foaas.herokuapp.com/life/Phil
>>> print fucking.text
Fuck my life. - Phil
```

Give me some random fucking things:

```
>>> print fuck.random(from_='Chris').text
Fuck you very much. - Chris
>>> print fuck.random(from_='Chris').text
Fuck my life. - Chris
>>> print fuck.random(name='Tom', from_='Chris').text
Fuck me gently with a chainsaw, Tom. Do I look like Mother Teresa? - Chris
>>> print fuck.random(name='Tom', from_='Chris').text
Fuck off, Tom. - Chris
```

### Supported Actions

   * `fuck.anyway(company, from_)`
   * `fuck.asshole(from_)`
   * `fuck.awesome(from_)`
   * `fuck.back(name, from_)`
   * `fuck.bag(from_)`
   * `fuck.ballmer(name, company, from_)`
   * `fuck.bday(name, from_)`
   * `fuck.because(from_)`
   * `fuck.blackadder(name, from_)`
   * `fuck.bm(name, from_)`
   * `fuck.bucket(from_)`
   * `fuck.bus(name, from_)`
   * `fuck.bye(from_)`
   * `fuck.caniuse(tool, from_)`
   * `fuck.chainsaw(name, from_)`
   * `fuck.cocksplat(name, from_)`
   * `fuck.cup(from_)`
   * `fuck.cool(from_)`
   * `fuck.dalton(name, from_)`
   * `fuck.deraadt(name, from_)`
   * `fuck.diabetes(from_)`
   * `fuck.donut(name, from_)`
   * `fuck.dosomething(do, something, from_)`
   * `fuck.equity(name, from_)`
   * `fuck.even(from_)`
   * `fuck.everyone(from_)`
   * `fuck.everything(from_)`
   * `fuck.family(from_)`
   * `fuck.fascinating(from_)`
   * `fuck.fewer(name, from_)`
   * `fuck.field(name, from_, reference)`
   * `fuck.flying(from_)`
   * `fuck.ftfy(from_)`
   * `fuck.fts(name, from_)`
   * `fuck.fyyff(from_)`
   * `fuck.gfy(name, from_)`
   * `fuck.give(from_)`
   * `fuck.greed(noun, from_)`
   * `fuck.holygrail(from_)`
   * `fuck.horse(from_)`
   * `fuck.idea(from_)`
   * `fuck.immensity(from_)`
   * `fuck.ing(name, from_)`
   * `fuck.jinglebells(from_)`
   * `fuck.keep(name, from_)`
   * `fuck.keepcalm(reaction, from_)`
   * `fuck.king(name, from_)`
   * `fuck.legend(name, from_)`
   * `fuck.life(from_)`
   * `fuck.linus(name, from_)`
   * `fuck.logs(from_)`
   * `fuck.look(name, from_)`
   * `fuck.looking(from_)`
   * `fuck.madison(name, from_)`
   * `fuck.maybe(from_)`
   * `fuck.me(from_)`
   * `fuck.mornin(from_)`
   * `fuck.no(from_)`
   * `fuck.nugget(name, from_)`
   * `fuck.off(name, from_)`
   * `fuck.off-with(behavior, from_)`
   * `fuck.outside(name, from_)`
   * `fuck.particular(thing, from_)`
   * `fuck.pink(from_)`
   * `fuck.problem(name, from_)`
   * `fuck.programmer(from_)`
   * `fuck.pulp(language, from_)`
   * `fuck.question(from_)`
   * `fuck.ratsarse(from_)`
   * `fuck.retard(from_)`
   * `fuck.ridiculous(from_)`
   * `fuck.rockstar(name, from_)`
   * `fuck.rtfm(from_)`
   * `fuck.sake(from_)`
   * `fuck.shakespeare(name, from_)`
   * `fuck.shit(from_)`
   * `fuck.shutup(name, from_)`
   * `fuck.single(from_)`
   * `fuck.thanks(from_)`
   * `fuck.that(from_)`
   * `fuck.think(name, from_)`
   * `fuck.thinking(name, from_)`
   * `fuck.this(from_)`
   * `fuck.thumbs(name, from_)`
   * `fuck.too(from_)`
   * `fuck.tucker(from_)`
   * `fuck.waste(name, from_)`
   * `fuck.what(from_)`
   * `fuck.xmas(name, from_)`
   * `fuck.yoda(name, from_)`
   * `fuck.you(name, from_)`
   * `fuck.zayn(from_)`
   * `fuck.zero(from_)`

### tl;dr

```
foaas.Fuck([secure=True]).<action>(**kwargs)[.<url|html|text|json>]
```

Testing
-------

```
$ python tests.py
.......
----------------------------------------------------------------------
Ran 7 tests in 0.724s

OK
```

... or use [tox]:

```
$ tox
```

[FOAAS]: http://foaas.com/
[Derek Payton]: http://dmpayton.com
[MIT]: https://github.com/dmpayton/foaas-python/blob/master/LICENSE
[requests]: http://python-requests.org/
[pip]: http://www.pip-installer.org/
[tox]: https://tox.readthedocs.org/
