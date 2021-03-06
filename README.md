This is a manually-maintained index to Unity installer releases.
It is intended to be used for performing automated installation of the Unity client.

You can browse the repository at <https://github.com/falldamagestudio/UnityDownloadURLs>.

You can access the results at <https://falldamagestudio.github.io/UnityDownloadURLs>.

# How to use

First, determine which version of Unity that you want. Then, fetch an index of available installers for that version. Finally, fetch the installers that you need.

## Get the latest version number

You can get the version number of the latest release - a major version, a minor version, or a beta - by visiting the following URLs:

<https://falldamagestudio.github.io/UnityDownloadURLs/versions/2018.2-latest/Windows64>

<https://falldamagestudio.github.io/UnityDownloadURLs/versions/2018-latest/Windows64>

<https://falldamagestudio.github.io/UnityDownloadURLs/versions/beta-latest/Windows64>

Each of the URLs will return a raw version string, such as `2018.2.5f1`.

## Construct a download URL

Installer indices for each version of Unity will be on the format: <https://falldamagestudio.github.io/UnityDownloadURLs/installers/{version}.json>

A version number is typically on the form of `2018.2.5f1`. For example, <https://falldamagestudio.github.io/UnityDownloadURLs/installers/2018.2.5f1.json> is a valid installer index.

Accessing an installer index will return a JSON blob which might look like this:

```
{
	"Windows64-AndroidTargetSupport" : "http://beta.unity3d.com/download/3f0ac31c6d6f/TargetSupportInstaller/UnitySetup-Android-Support-for-Editor-2018.3.0b1.exe",
	"Windows64-AppleTVTargetSupport" : "http://beta.unity3d.com/download/3f0ac31c6d6f/TargetSupportInstaller/UnitySetup-AppleTV-Support-for-Editor-2018.3.0b1.exe",
	"Windows64-Documentation" : "http://beta.unity3d.com/download/3f0ac31c6d6f/WindowsDocumentationInstaller/UnityDocumentationSetup.exe",
	"Windows64-Editor" : "http://beta.unity3d.com/download/3f0ac31c6d6f/Windows64EditorInstaller/UnitySetup64.exe",
	"Windows64-FacebookGamesTargetSupport" : "http://beta.unity3d.com/download/3f0ac31c6d6f/TargetSupportInstaller/UnitySetup-Facebook-Games-Support-for-Editor-2018.3.0b1.exe",
	"Windows64-iOSTargetSupport" : "http://beta.unity3d.com/download/3f0ac31c6d6f/TargetSupportInstaller/UnitySetup-iOS-Support-for-Editor-2018.3.0b1.exe",
	"Windows64-LinuxTargetSupport" : "http://beta.unity3d.com/download/3f0ac31c6d6f/TargetSupportInstaller/UnitySetup-Linux-Support-for-Editor-2018.3.0b1.exe",
	"Windows64-MacOSMonoTargetSupport" : "http://beta.unity3d.com/download/3f0ac31c6d6f/TargetSupportInstaller/UnitySetup-Mac-Mono-Support-for-Editor-2018.3.0b1.exe",
	"Windows64-VuforiaTargetSupport" : "http://beta.unity3d.com/download/3f0ac31c6d6f/TargetSupportInstaller/UnitySetup-Vuforia-AR-Support-for-Editor-2018.3.0b1.exe",
	"Windows64-WebGLTargetSupport" : "http://beta.unity3d.com/download/3f0ac31c6d6f/TargetSupportInstaller/UnitySetup-WebGL-Support-for-Editor-2018.3.0b1.exe",
	"Windows64-WindowsIL2CPPTargetSupport" : "http://beta.unity3d.com/download/3f0ac31c6d6f/TargetSupportInstaller/UnitySetup-Windows-IL2CPP-Support-for-Editor-2018.3.0b1.exe",
	"Windows64-WindowsStoreIL2CPPTargetSupport" : "http://beta.unity3d.com/download/3f0ac31c6d6f/TargetSupportInstaller/UnitySetup-UWP-IL2CPP-Support-for-Editor-2018.3.0b1.exe",
	"Windows64-WindowsStoreNETTargetSupport" : "http://beta.unity3d.com/download/3f0ac31c6d6f/TargetSupportInstaller/UnitySetup-UWP-.NET-Support-for-Editor-2018.3.0b1.exe"
}
```

Which components exist varies between major Unity releases; the editor is usually called `Windows64-Editor`. 

You can extract the download URLs that you need from the JSON blob. Fetch the installers with `wget` or similar.

# Updating the index

This index is updated manually. Pull requests to the GitHub repo are welcome!