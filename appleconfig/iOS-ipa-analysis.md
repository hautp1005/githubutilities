# `ipa` package analysis

`ipa` is essentially a `zip` file.

# `ipa` file root structures

* `iTunes Artwork`--a PNG app icon for showing in iTunes and the App Store.
* `iTunesMetadata.plist`—Contains copyright information, release date, purchase date, name of the developer and company who created it, etc.
* `/Payload/Application.app`

> To repack the `ipa`, simple select the three files and folder listed above and right click and select compress. The `Archive.zip` you get can be install using `ideviceinstaller`. You can also rename the file name you wanted.

> You can also use script.

```sh
cd <the-directory-that-store-the-three-files-and-folder>
zip -0 -y -r out.ipa .
#or use
zip -0  --symlinks --recurse-paths out.ipa .
# the `out.ipa` is the result
```


# What in the `Payload`

* `_CodeSignature/CodeResources`—-configuration file for `app` in the  `Payload` resources, which is a xml configuration file. It includes two keys—`files` and `rules`. It can be thought as an index for files in the `app`.
* `PkgInfo`--It belongs to `files` in `CodeResources` config. The contents of the PkgInfo file are the 4-byte package type followed by the 4-byte signature of your application. It comes from OS X and is not required by iOS. For more info, please refer to [here](https://developer.apple.com/library/mac/documentation/MacOSX/Conceptual/BPRuntimeConfig/Articles/ConfigApplications.html).
* `*.nib`—-compiled views
* `*.strings`—-apple binary property list for storing localizable strings
* `embedded.mobileprovision`--embeded provisioning profile
* `*.lproj`--for localization usage
* `Info.plist`--contains info about where to launch application, MinimumOSVersion, etc.


## Reference

* [IPA files – Apple’s proprietary format for archive files for Iphone Ipod Touch and Ipad applications – Uses Apple’s FairPlay DRM technology](https://apttech.wordpress.com/2011/12/30/ipa-files-apples-proprietary-format-for-archive-files-for-iphone-applications-uses-apples-fairplay-drm-technology/)
* [[HOW TO] Edit iTunes apps (IPA files) to be installed on unsupported devices](http://www.ifans.com/forums/threads/how-to-edit-itunes-apps-ipa-files-to-be-installed-on-unsupported-devices.370037/)
* [The iTunesMetadata.plist on xamarin.com File](http://developer.xamarin.com/guides/ios/deployment,_testing,_and_metrics/app_distribution_overview/itunesmetadata/)
* [gist for unpack ipa metadata](https://gist.github.com/niw/5971209)
* [install `ipa` on jailbroken device](http://apple.stackexchange.com/questions/7068/how-can-i-manually-install-applications-on-a-jailbroken-ipad)
