소개
-----

  node.js 알짜배기 문서제공하고, Node.js Black Edition의 Helper로서 동작하는데 목적이 있습니다. github의 readme를 긁어와서 바로 보여줄 수 있지만, 내가 사용해보고 중요한 부분을 color module을 사용하여 제공합니다. 문서의 업데이트는 module 중요도에 따라 계속 쭈~욱 된다는것을 약속드립니다.
  
  
동기
-------

  리눅스에는 유명한 man 명령어가 있습니다. Node.js 에도 필요하지 않을까? 생각을 하자마자 프로젝트를 진행하기 시작했습니다.


설치
-----

    npm install nodeman -g

업데이트
--------

    npm update nodeman -g


문서추가 방법
--------------

- github에 README에 기재된 모든 내용보다는 필수적인 요소만 추출하고, 중요한 부분은 색상을 입혀서 작업시에 유용하게 참고할 수 있도록 작성해야 합니다.
- docs 디렉토리안에 public_<code>moduleName</code>_doc.js 규칙으로 생성되어야 합니다.
- <code>public_</code> 붙지 않은것은 node.js black edition의 NativeModule입니다. (nodeman -b 에서 구분목록 표시하기 위함)
- 파일의 내용은

        exports.name = 'moduleName';
        exports.context = 'use require';
        exports.homepage = 'http://homepage';
        exports.description = [
            "\t blah blah"
            , "\t blah blah"
        ].join('\n');



사용방법
----------

## cli

### $ nodeman -h
![usage](https://github.com/nanha/nodeman/raw/master/images/nodeman_usage.png)

### $ nodeman -b
![builtin](https://github.com/nanha/nodeman/raw/master/images/nodeman_builtin_list.png)

### $ nodeman optimist | more
![output](https://photos-1.dropbox.com/btj/4faa6d69/wrJ7qPsDFgAg78-vcNjiIR_GcUqX9rJvkD8n7y2Q7ks/ScreenShot003.jpg?size=1280x960)


## repl

    $ node
    > var man = require('nodeman');
    > man.help('optimist')


