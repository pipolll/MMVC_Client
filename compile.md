nuitka --standalone --mingw64 --follow-imports --windows-icon-from-ico=D:\GitRepository\RT-MMVC_Client\use_exe.ico --include-module=soundfile --include-package-data=librosa --include-package-dat==llvmlite --include-package-data=resampy --plugin-enable=tk-inter --plugin-enable=torch --plugin-enable=anti-bloat --plugin-enable=numpy --plugin-enable=multiprocessing --assume-yes-for-downloads --user-plugin=D:\GitRepository\RT-MMVC_Client\python\FixBuildPlugin_pytorch.py --include-plugin-directory=D:\GitRepository\RT-MMVC_Client\python --nofollow-import-to=torchvision --no-prefer-source-code D:\GitRepository\RT-MMVC_Client\python\mmvc_client_GPU.py

1)_soundfile_data\... がないといわれるので、pythonの環境から_soundfile_dataディレクトリを直接持ってくる
2)llvmlite.dll がないといわれるので、pythonの環境からllvmliteディレクトリを直接持ってくる
3)librosa\... がないといわれるので、
4)cannot load filter definition for kaiser best と言われるので、python環境から、resampyを持ってくる
5).distディレクトリにLibrary/bin/フォルダを作る（3.8以降参照される）
6)_sounddevice\... がないといわれるので、pythonの環境から_sounddevice_dataディレクトリを直接持ってくる


nuitka --standalone --mingw64 --follow-imports --windows-icon-from-ico=D:\GitRepository\RT-MMVC_Client\use_exe.ico --assume-yes-for-downloads --no-prefer-source-code D:\GitRepository\RT-MMVC_Client\python\output_audio_device_list.py

nuitka --standalone --mingw64 --follow-imports --windows-icon-from-ico=D:\GitRepository\RT-MMVC_Client\use_exe.ico --include-module=sounddevice --plugin-enable=tk-inter --plugin-enable=numpy --assume-yes-for-downloads --no-prefer-source-code D:\GitRepository\RT-MMVC_Client\python\rec_environmental_noise.py
