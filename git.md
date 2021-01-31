##### git文件修改机制

```
git对公共部分保留指针，对修改部分进行存储。
```





#### git 分支

```
作用: 紧急修复bug，环境隔离。
1.master: 主干线(一般是已经上线的分支)
2.自定义分支: 如Dev，bug

分支开发后合并
```

```
查看分支
git branch: 默认为 * master,* 后的分支代表所在的分支线
```

```
创建分支
git branch + 分支名
```

```
切换分支
git checkout 分支名

$ git checkout dev
Switched to branch 'dev'

各分支之间开发相互不影响
```

```
合并分支
1.切换回想要最终归并的主分支(如master)
2.git merge + 分支名
```

```
删除无用分支
git branch -d + 分支名

$ git branch -d dev
Deleted branch dev (was 97b8af3).
```

```
冲突解决:
手动打开文件进行增删改查

产生冲突的一般情况:
D = A + B ===> 分支1
E = A + C ===> 分支2
此时合并D、E会产生冲突，git不知道如何权衡去留

```

> 示意图

![](C:\Users\XUWL\Pictures\pic.png)

##### git 工作流

```
git写代码全在dev分支上实现，master上永远是线上稳定版，当dev成熟时再合并到master
```



![](C:\Users\XUWL\Pictures\azhe.png)



##### github使用

```
1.注册账号
2.创建仓库
3.本地代码推送(和本地相同，分支也会保留)
	3.1 git add remote origin(别名) url // 给url取别名
	3.2 git push -u origin + 分支名 // 推送代码
4.代码下载
	4.1 git clone + url
```

