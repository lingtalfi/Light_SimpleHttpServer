Light_SimpleHttpServer
===========
2020-10-30 -> 2021-03-22



A simple http server, which converts your exceptions into http responses with error status codes.


This is a [Light plugin](https://github.com/lingtalfi/Light/blob/master/doc/pages/plugin.md).

This is part of the [universe framework](https://github.com/karayabin/universe-snapshot).


Install
==========
Using the [planet installer](https://github.com/lingtalfi/Light_PlanetInstaller) via [light-cli](https://github.com/lingtalfi/Light_Cli)
```bash
lt install Ling.Light_SimpleHttpServer
```

Using the [uni](https://github.com/lingtalfi/universe-naive-importer) command.
```bash
uni import Ling/Light_HttpError
```

Or just download it and place it where you want otherwise.






Summary
===========
- [Light_HttpError api](https://github.com/lingtalfi/Light_SimpleHttpServer/blob/master/doc/api/Ling/Light_HttpError.md) (generated with [DocTools](https://github.com/lingtalfi/DocTools))
- [Services](#services)
- Pages
    - [Conception notes](https://github.com/lingtalfi/Light_SimpleHttpServer/blob/master/doc/pages/conception-notes.md)
    - [Events](https://github.com/lingtalfi/Light_SimpleHttpServer/blob/master/doc/pages/events.md)






Services
=========


Here is an example of the service configuration:

```yaml
simple_http_server:
    instance: Ling\Light_SimpleHttpServer\Service\LightSimpleHttpServerService
    methods:
        setContainer:
            container: @container()
        setOptions:
            options:
                do_not_log_codes:
                    - 404
                    - 403





```



History Log
=============

- 1.0.13 -- 2021-05-31

    - Removing trailing plus in lpi-deps file (to work with Light_PlanetInstaller:2.0.0 api

- 1.0.12 -- 2021-05-03

    - Update dependencies to Ling.Light_Events (pushed by SubscribersUtil)

- 1.0.11 -- 2021-05-03

    - Update dependencies to Ling.Light_Events (pushed by SubscribersUtil)

- 1.0.10 -- 2021-05-03

    - Update dependencies to Ling.Light_Events (pushed by SubscribersUtil)

- 1.0.9 -- 2021-03-22

    - fix events not namespaced correctly
  
- 1.0.8 -- 2021-03-15

    - update planet to adapt Ling.Light:0.70.0

- 1.0.7 -- 2021-03-05

    - update README.md, add install alternative

- 1.0.6 -- 2020-12-08

    - Fix lpi-deps not using natsort.

- 1.0.5 -- 2020-12-04

    - Add lpi-deps.byml file

- 1.0.4 -- 2020-11-20

    - rename repository to Light_SimpleHttpServer, as Light_HttpError was confusing
    
- 1.0.3 -- 2020-10-30

    - fix LightHttpErrorController->render using non strict version of in_array for checking "not send logs"
    
- 1.0.2 -- 2020-10-30

    - update service, now can choose which http status codes to not send to the log
    
- 1.0.1 -- 2020-10-30

    - fix LightHttpErrorController->doRender being public instead of protected
    
- 1.0.0 -- 2020-10-30

    - initial commit