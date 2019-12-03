Metadata 是PHP中用于类/方法/属性元数据管理的数据库
==========================================================================

| [Master (2.x)][Master] | [1.x][1.x] |
|:----------------:|:----------:|
| [![Build status][Master image]][Master] | [![Build status][1.x image]][1.x] |
| [![Coverage Status][Master coverage image]][Master coverage] | [![Coverage Status][1.x coverage image]][1.x coverage] |


概述
--------

这个库提供了一些管理元数据所需的常用基类用于类、方法和属性。
元数据可以来自许多不同的地方。
元数据类用于抽象出源代码并提供一个公共的所有这些的接口。

使用
-----

这个库提供了三个类，您可以扩展它们来添加您的应用程序特定的属性和标志：  
``ClassMetadata``, ``MethodMetadata``, 和``PropertyMetadata``

添加完子类中的属性后，还需要添加 ``DriverInterface`` 知道如何填充这些类的实现来自不同的元数据源。

最后，您可以使用 ``MetadataFactory`` 去检索元数据::

```php
<?php

use Metadata\MetadataFactory;
use Metadata\Driver\DriverChain;

$driver = new DriverChain(array(
    /** Annotation, YAML, XML, PHP, ... drivers */
));
$factory = new MetadataFactory($driver);
$metadata = $factory->getMetadataForClass('MyNamespace\MyObject');
```  

  [Master image]: https://img.shields.io/travis/schmittjoh/metadata/master.svg?style=flat-square
  [Master]: https://travis-ci.org/schmittjoh/metadata
  [Master coverage image]: https://img.shields.io/scrutinizer/coverage/g/schmittjoh/metadata/master.svg?style=flat-square
  [Master coverage]: https://scrutinizer-ci.com/g/schmittjoh/metadata/?branch=master

  [1.x image]: https://img.shields.io/travis/schmittjoh/metadata/1.x.svg?style=flat-square
  [1.x]: https://github.com/schmittjoh/metadata/tree/1.x
  [1.x coverage image]: https://img.shields.io/scrutinizer/coverage/g/schmittjoh/metadata/1.x.svg?style=flat-square
  [1.x coverage]: https://scrutinizer-ci.com/g/schmittjoh/metadata/?branch=1.x
