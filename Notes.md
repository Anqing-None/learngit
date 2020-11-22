# 分支
在每一次commit都会创建一个commit ID
默认分支master会指向这个ID
而Git中还有一个指针HEAD，HEAD不指向提交，而是指向当前分支
创建一个名为dev的新分支时，dev指向master相同的commit ID，HEAD指向dev则表示在当前分支上
假设dev领先几个commit，只需要将master指向dev指向的commt即可，就可完成两个分支的合并；

## 实战

创建dev分支
''' git checkout -b dev 
    -b 表示创建并切换到改分支；
    等价于==》
    git branch dev
    git checkout dev

'''
在dev分支commit后文件返回master文件状态会回到master

merge
在master分支上使用git merge dev可以将commit到dev分支的文件状态恢复
这步操作相当于将master指针指向dev

merge后删除dev分支

''' git branch -d dev '''
