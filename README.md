# Domain Driven Design

## Intall basic Laravel Application

*  Via Composer 

```git
 $ composer create-project laravel/laravel example-app
```
* Or via globle installed command

```git
 $ laravel new app-name
```

## Change autoload psr-4 property acording to your folder stucture in composer.json (EX: )

```git
 "psr-4": {
      "App\\": "src/app/",
      "Domain\\": "src/domain/",
      "Support\\": "src/support/"
  }
```

## Move app folder acordig to folder stucture you defined in composer.json

## Create a class inside app directory. Name is up to you (Recomended: Name it similar to your application name) 

```git
  class TestApp extends Application
  {
      protected $appPath = __DIR__;

      protected $namespace = 'App\\';

      protected $domain = 'Domain\\';
  }
```

## Extends the Illuminate\Foundation\Application and add app path + namespace

```git
  <?php

  namespace App;

  use Illuminate\Foundation\Application;

  class TestApp extends Application
  {
    protected $appPath = __DIR__;

    protected $namespace = 'App\\';

    protected $domain = 'Domain\\';
  }
```


## Finally dump the composer

```git
  $ composer dump-autoload
```


## Your app is good to go 🤙

```git
  $ Happy coding 💻
```
