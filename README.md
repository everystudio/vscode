# vscode
vscode

- Unity終了時に強制終了が発生する場合の対応

static void FixUnityPreferences()内にある

if ( EditorWindow.focusedWindow == null)
return;

を


if ( !EditorApplication.isPlaying || EditorWindow.focusedWindow == null)
return;

とすれば直る。
