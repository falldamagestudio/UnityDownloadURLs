This is a manually-maintained index to Unity installer releases.
It is intended to be used for performing automated installation of the Unity client.

You can browse the repository at <https://github.com/falldamagestudio/UnityDownloadURLs>.
You can access the results at <falldamagestudio.github.io/UnityDownloadURLs>.

# How to use

First, determine which version of Unity that you want. Then, construct a download URL and fetch the files from there.

## Get latest version number

You can get the version number of the latest release - a major version, a minor version, or a beta - by visiting the following URLs:

<https://falldamagestudio.github.io/UnityDownloadURLs/versions/2018.2-latest/Windows64>

<https://falldamagestudio.github.io/UnityDownloadURLs/versions/2018-latest/Windows64>

<https://falldamagestudio.github.io/UnityDownloadURLs/versions/beta-latest/Windows64>

## Construct a download URL

Download URLs will be on the format:

https://falldamagestudio.github.io/UnityDownloadURLs/installers/{version}/{component}

A version number is typically on the form of `2018.2.5f1`. Which components exist varies between major Unity releases; the editor is usually called `Windows64-Editor`.

You can fetch this URL with `wget` or similar. It will HTTP-REFRESH redirect to the real file on Unity's site (netstorage.unity3d.com).

# Updating index

This index is updated manually. Pull requests to the GitHub repo are welcome!