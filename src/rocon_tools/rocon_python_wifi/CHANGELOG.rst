Changelog
=========

0.1.23 (2015-07-13)
-------------------

0.1.22 (2015-07-13)
-------------------

0.1.21 (2015-07-09)
-------------------

0.1.20 (2015-06-01)
-------------------

0.1.19 (2015-05-27)
-------------------

0.1.18 (2015-05-06)
-------------------
* Don't fail on wifi-if check for different systems
  In wifi part of detection of network interfaces: Check if /proc/net/wireless exists before trying to read it, instead of failing on OS's / systems that don't have wifi and/or don't use that file.
* Contributors: Rob Linsalata

0.1.17 (2015-04-06)
-------------------

0.1.16 (2015-03-02)
-------------------

0.1.15 (2015-02-27)
-------------------

0.1.14 (2015-02-09)
-------------------

0.1.13 (2015-01-12)
-------------------

0.1.12 (2015-01-08)
-------------------

0.1.11 (2014-12-02)
-------------------

0.1.10 (2014-11-21)
-------------------

0.1.9 (2014-08-25)
------------------
* move from symbolic links to includes for changelogs to avoid eclipse bewilderment.
* Contributors: Daniel Stonier

0.1.6 (2014-05-06)
------------------
* bugfix install rule of original documentation notes.
* maintainer correctly added.
* Contributors: Daniel Stonier

0.1.5 (2014-05-05)
------------------
* sphinx documentation added.
* Contributors: Daniel Stonier

0.1.0 (2014-03-31)
------------------
* rocon_python_wifi moved here from `rocon_multimaster`_
* Contributors: Daniel Stonier

.. _`rocon_multimaster`: https://github.com/robotics-in-concert/rocon_multimaster
