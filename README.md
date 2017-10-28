| Windows | Linux | OS X |
| :---- | :------ | :---- |
[![Windows build status][1]][2] | [![Linux build status][3]][4] | [![OS X build status][5]][6] | 

[1]: https://ci.appveyor.com/api/projects/status/j9g1kfpo48kf3eyr?svg=true
[2]: https://ci.appveyor.com/project/breezehubadmin/breeze
[3]: https://travis-ci.org/BreezeHub/Breeze.svg?branch=tumblebit-alpha
[4]: https://travis-ci.org/BreezeHub/Breeze
[5]: https://travis-ci.org/BreezeHub/Breeze.svg?branch=tumblebit-alpha
[6]: https://travis-ci.org/BreezeHub/Breeze


# Breeze

__Warning: This is an experimental build. At the moment, only bitcoin on testnet is supported but more is coming soon. Use at your own risk.__
This is the repository of the Breeze Wallet, the first full-block SPV bitcoin wallet using Angular and Electron at the front-end and C# with .NET Core in the back-end.

## Daemon Build

Breeze daemon is the backend REST service, hosting a Bitcoin node upon which Breeze UI depends:

```
# Clone and go in the directory
git clone https://github.com/breezehub/Breeze
cd Breeze

# Initialize dependencies
git submodule update --init --recursive

# Go in the Breeze deamon folder
cd StratisBitcoinFullNode/Stratis.BreezeD
dotnet build

# Run the Bitcoin and Stratis full-SPV daemons on testnet in separate terminals
dotnet run -testnet
dotnet run stratis -testnet
```

## UI Build

[Read more...](https://github.com/stratisproject/Breeze/blob/master/Breeze.UI/README.md)

## CI Build
-----------

We use [AppVeyor](https://www.appveyor.com/) for Windows CI builds and [Travis CI](https://travis-ci.org/) (coming soon) for our Linux and MacOS ones.
Every time someone pushes to the master branch or create a pull request on it, a build is triggered and a new unstable app release is created.

To skip a build, for example if you've made very minor changes, include the text **[skip ci]** or **[ci skip]** in your commits' comment (with the squared brackets).

If you want the :sparkles: latest :sparkles: (unstable :bomb:) version of the Breeze app, you can get it here: 

|    | x86 Release | x64 Release | Notes |
|:---|----------------:|------------------:|------------------:|
|**Windows 7**| [download][7] | [download][8] | continuous build - up to date with commits |
|**Windows 10**| [download][9] | [download][10] | continuous build - up to date with commits | 
|**Ubuntu 14.04**| - | [download][11] | continuous build - up to date with commits |
|**OS X 10.12**| - | [download][14] |  continuous build - up to date with commits |

This is early release, alpha software, is provided for experiment, testing and development purposes and should only be used on **testnet**.

For **testnet** only.

[7]: https://ci.appveyor.com/api/projects/breezehubadmin/breeze/artifacts/breeze_out/breeze-win7-x86-Release.zip?job=Environment%3A%20win_runtime%3Dwin7-x86%2C%20arch%3Dia32%2C%20plat%3Dwin32
[8]: https://ci.appveyor.com/api/projects/breezehubadmin/breeze/artifacts/breeze_out/breeze-win7-x64-Release.zip?job=Environment%3A%20win_runtime%3Dwin7-x64%2C%20arch%3Dx64%2C%20plat%3Dwin32
[9]: https://ci.appveyor.com/api/projects/breezehubadmin/breeze/artifacts/breeze_out/breeze-win10-x86-Release.zip?job=Environment%3A%20win_runtime%3Dwin10-x86%2C%20arch%3Dia32%2C%20plat%3Dwin32
[10]: https://ci.appveyor.com/api/projects/breezehubadmin/breeze/artifacts/breeze_out/breeze-win10-x64-Release.zip?job=Environment%3A%20win_runtime%3Dwin10-x64%2C%20arch%3Dx64%2C%20plat%3Dwin32
[11]: https://github.com/breezehub/Breeze/releases/download/cd-unstable/breeze-ubuntu.14.04-x64-Release.zip
[12]: https://github.com/breezehub/Breeze/releases/download/cd-unstable/breeze-ubuntu.14.04-x64-Release.zip
[13]: https://github.com/breezehub/Breeze/releases/download/cd-unstable/breeze-osx.10.11-x64-Release.zip
[14]: https://github.com/breezehub/Breeze/releases/download/cd-unstable/breeze-osx.10.12-x64-Release.zip

With TumbleBit
