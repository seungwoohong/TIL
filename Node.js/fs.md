# fs
Node fs module에 대한 내용의 문서이다.
이 문서는 계속적으로 업데이트 될 것 이다

### File System
```
var fs = require('fs');
```

* fs.readdir(path,[callback])

비동기로 디렉토리의 내용을 읽는다. 콜백은 두개의 인자를 받는다. (err, files)는 디렉토리에서 '.', '..' 즉, 현재 폴더와 상위폴더를 제외한 하위 폴더의 파일, 디렉토리들 이름의 배열이다.

```
fs.readdir('url',(err, files) => {
    if(err) throw err;

    console.log(files);
});
```

* fs.readdirSync(path)
동기적으로 '.' 와 '..'를 제외한 하위 디렉토리와 파일명들의 배열을 반환함

```
var files = fs.readdir('url');
console.log(files);
```
