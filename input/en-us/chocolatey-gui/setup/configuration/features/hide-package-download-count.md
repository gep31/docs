---
Order: 120
xref: hide-package-download-count
Title: Hide Package Download Count
Description: Allows control over whether package download count is displayed on remote source views.
---

By default, Chocolatey GUI will attempt to show the download statistics for a package on a remote feed.  This can be
useful when making a decision about whether to install a package or not.  For example, when viewing the Chocolatey
Community Repository feed, you will see the following:

![Hide Package Download Count Disabled 1](/assets/images/chocolatey-gui/feature_hide_package_download_count_disabled_1.png "Hide Package Download Count Disabled 1")

However, when using a feed that doesn't support package download statistics, you can be shown the following which isn't
as useful:

![Hide Package Download Count Disabled 2](/assets/images/chocolatey-gui/feature_hide_package_download_count_disabled_2.png "Hide Package Download Count Disabled 2")

By enabling this feature, you can turn off package download count for all sources, and as a result, you will see the
following:

![Hide Package Download Count Enabled 1](/assets/images/chocolatey-gui/feature_hide_package_download_count_enabled_1.png "Hide Package Download Count Enabled 1")

![Hide Package Download Count Enabled 2](/assets/images/chocolatey-gui/feature_hide_package_download_count_enabled_2.png "Hide Package Download Count Enabled 2")

> :memo: **NOTE**
>
> It is currently not possible to configure showing/hiding the package download count for individual feeds

## Resources

Below is a short video which shows this feature in action:

<p>
<div class="ratio ratio-16x9">
    <iframe src="https://www.youtube.com/embed/W8kTjbKTHj8?list=PL84yg23i9GBjAMY0OfHfn-MH4rviaccuc" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen>
    </iframe>
</div>
<br>
</p>

## Example

This feature can be enabled, for the currently logged in user, by running the following command:

```powershell
chocolateyguicli feature enable --name="'HidePackageDownloadCount'"
```

This feature can be disabled, for the currently logged in user, by running the following command:

```powershell
chocolateyguicli feature disable --name="'HidePackageDownloadCount'"
```

Or, to enable/disable it globally at the machine level, run the following commands:

```powershell
chocolateyguicli feature enable --name="'HidePackageDownloadCount'" --global

chocolateyguicli feature disable --name="'HidePackageDownloadCount'" --global
```

## Default Value

The default value for this feature is disabled.

## Availability

The ability to control this feature from the Chocolatey GUI Settings screen has existed since Chocolatey GUI v0.17.0.

The ability to control this feature from the command line using `chocolateyguicli` has existed since Chocolatey GUI
v0.17.0.
