# GIT 오류사항_220803

```bash
PC이름@DESKTOP-ABRUF8O MINGW64 /d/김민채/개인/코딩공부
$ git pull origin master
fatal: not a git repository (or any of the parent directories): .git
```

* repository 설정 없이 바로 git pull부터 입력해서 오류

```bash
PC이름@DESKTOP-ABRUF8O MINGW64 /d/김민채/개인/코딩공부
$ git init
Initialized empty Git repository in D:/김민채/개인/코딩공부/.git/
```

```bash
PC이름@DESKTOP-ABRUF8O MINGW64 /d/김민채/개인/코딩공부 (master)
$ git pull
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=<remote>/<branch> master

```

```bash
PC이름@DESKTOP-ABRUF8O MINGW64 /d/김민채/개인/코딩공부 (master)
$ git remote add origin https://github.com/chaechaeno1/Vim.git
```

* repository 주소 원격 연결

```bash
PC이름@DESKTOP-ABRUF8O MINGW64 /d/김민채/개인/코딩공부 (master)
$ git pull
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 3 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 718 bytes | 9.00 KiB/s, done.
From https://github.com/chaechaeno1/Vim
 * [new branch]      master     -> origin/master
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> master

```

* 계속 upstream 하라고 함

```bash
PC이름@DESKTOP-ABRUF8O MINGW64 /d/김민채/개인/코딩공부 (master)
$ git remote -v // '원격저장소 이름 확인'
origin  https://github.com/chaechaeno1/Vim.git (fetch)
origin  https://github.com/chaechaeno1/Vim.git (push)
```

```bash
PC이름@DESKTOP-ABRUF8O MINGW64 /d/김민채/개인/코딩공부 (master)
$ git pull
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> master
```

* 벌써 오류 세번째임

```bash
PC이름@DESKTOP-ABRUF8O MINGW64 /d/김민채/개인/코딩공부 (master)
$ git push origin master
error: src refspec master does not match any
error: failed to push some refs to 'https://github.com/chaechaeno1/Vim.git'
```

* pull 해야 할 걸 push라고 입력해서 오류 뜸

```bash
PC이름@DESKTOP-ABRUF8O MINGW64 /d/김민채/개인/코딩공부 (master)
$ git pull origin master
From https://github.com/chaechaeno1/Vim
 * branch            master     -> FETCH_HEAD
```

* 드디어 pull 성공!!