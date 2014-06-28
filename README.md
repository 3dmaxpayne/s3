yii2-s3-upload
==============

This extension provides upload to S3 files in Yii Framework 2.
It is a wrapper for AWS SDK for PHP (@link https://github.com/aws/aws-sdk-php)

## Installation

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
$ php composer.phar require mag/S3 "dev-master"
```

or add

```
"mag/S3": "dev-master"
```

to the ```require``` section of your `composer.json` file.

## Use

add in config:
```php
'components' => [
        's3' => [
            'class'     => 'mag/S3',
            'key'       => 'Your access key from amazon',
            'secret'    => 'Your secret key from amazon',
            'bucket'    => 'Bucket name',
        ],
        ...
```

And you can use it:
```php
\Yii::$app->s3->upload('/home/username/Pictures/P1010238.JPG', 'test/my.jpg');
```

first param is local file name
second param is file name on Amazon S3 server. It can include directories.