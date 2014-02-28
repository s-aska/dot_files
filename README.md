
## Setup

	ln -s dot_files/.zshenv .zshenv
	ln -s dot_files/.zshrc .zshrc
	ln -s dot_files/.tmux.conf .tmux.conf

### zsh / tmux or screen / plenv / rbenv の組みあせを使う場合以下のようにpath_helper実行前にPATHをクリアしないとPATHを壊される

	--- /etc/zshenv.orig
	+++ /etc/zshenv
	@@ -1,4 +1,5 @@
	 # system-wide environment settings for zsh(1)
	 if [ -x /usr/libexec/path_helper ]; then
	+ PATH=""
	  eval `/usr/libexec/path_helper -s`
	 fi