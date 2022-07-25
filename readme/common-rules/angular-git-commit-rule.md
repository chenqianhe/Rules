# \[Angular] Git Commit Rule

**Angular团队**制定的提交规范是目前市面上公认为最合理、最系统、最流行的提交规范`，`即使一目十行地扫视，也能得到每条提交说明的信息。



在git提交中应该有Header、Body、Footer，其中，Header是必要的，Body和Footer是选择性写的。

```
<type>(<scope>): <subject>
# 空一行
<body>
# 空一行
<footer>
```

### **Header**

该部分仅书写一行，包括三个字段，分别是type、scope和subject。

* **type**：用于说明 commit 的提交类型，必选
* **scope**：用于说明 commit 的影响范围，可选
* **subject**：用于说明 commit 的细节描述，可选

type 用于说明 commit 的提交类型，一般使用以下选项即可。

1. build：对构建系统或者外部依赖项进行了修改&#x20;
2. ci：对CI配置文件或脚本进行了修改&#x20;
3. docs：对文档进行了修改&#x20;
4. feat：增加新的特征&#x20;
5. fix：修复bug&#x20;
6. pref：提高性能的代码更改&#x20;
7. refactor：既不是修复bug也不是添加特征的代码重构&#x20;
8. style：不影响代码含义的修改，比如空格、格式化、缺失的分号等&#x20;
9. test：增加确实的测试或者矫正已存在的测试



scope 用于说明 commit 的影响范围，简要说明本次改动的影响范围。

subject 用于说明 commit 的细节描述。文字一定要精简精炼，同时尽量遵循以下规则。

* 以动词开头，使用第一人称现在时，比如change，而不是changed或changes
* 首个字母不能大写
* 结尾不能存在句号(.)

### **Body**

这部分是对本次提交的详细描述，可以分成多行。

* 使用第一人称现在时，比如使用 change 而不是 changed 或者 changes
* 说明代码变更的动机，以及和以前代码的对比

### Footer

只有两种情况：&#x20;

1. 不兼容变动：所有不兼容变动应该被列为不兼容变动块放在信息尾部，应该以“BREAKING CHANGE:”开始，后面是对变动的描述，以及变动的动机和迁移方法&#x20;
2. 引用讨论：如果当前提交是针对某个讨论，那么可以在尾部关闭这个讨论 Closes #234 或者同时关闭多个讨论 Closes #123, #245, #992

### 完全的提交示例：

```bash
git commit -m "fix(core): 修复了内核的一个xx bug" -m "此次修复了之前一直导致系统不稳定的问题" -m "关闭issue xx"
```

### 使用git-cz

{% embed url="https://github.com/commitizen/cz-cli" %}





