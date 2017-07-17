# SVN merge

1. check out trunk
```shell
svn co svn+ssh://server/path/trunk
```

2. check out branch
```shell
svn co svn+ssh://server/path/branch
```

3. find branch start version -> XXXX
```shell
cd branch
svn log --stop-on-copy
```

4. find trunk update version -> YYYY
``` shell
cd ../trunk
svn up
```

5. merge
```shell
svn merge -rXXXX:YYYY svn+ssh://server/path/branch
```

6. resolve conflict

7. commit
```ssh
svn ci -m 'MERGE branch to trunk'
```

