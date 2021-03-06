---

Description: 'DISM Windows PE Servicing Command-Line Options'
ms.assetid: d759221d-47ee-4f50-957e-3b978be22dea
MSHAttr: 'PreferredLib:/library/windows/hardware'
title: 'DISM Windows PE Servicing Command-Line Options'
ms.date: 01/07/2019
ms.topic: article

---

# DISM Windows PE Servicing Command-Line Options

You can update Windows Preinstallation Environment (WinPE) by adding drivers, language packs, list packages and prepare the Windows PE image for deployment.

You must use these commands on a mounted WinPE image. See [WinPE: Mount and Customize](winpe-mount-and-customize.md). These options cannot be used with an online, running version of Windows PE. 

In addition to the [DISM global options](dism-global-options-for-command-line-syntax.md), the following Windows PE servicing options are available. These options are not case sensitive.

**DISM.exe /Image:** *&lt;path\_to\_image\_directory&gt;* \[**/Get-PESettings** | **/Get-ScratchSpace** | **/Get-TargetPath** | **/Set-ScratchSpace:***&lt;size\_of\_ScratchSpace&gt;* | **/Set-TargetPath :***&lt;target\_path&gt;* \]


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Option</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>/Get-PESettings</strong></p></td>
<td align="left"><p>Displays a list of Windows PE settings in the Windows PE image. The list includes scratch space settings and target path settings. For example:</p>
<p><strong>Dism /image:C:\test\offline /Get-PESettings</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>/Get-ScratchSpace</strong></p></td>
<td align="left"><p>Retrieves the configured amount of Windows PE system volume scratch space. This setting represents the amount of writeable space available on the Windows PE system volume when booted in ramdisk mode. For example:</p>
<p><strong>Dism /image:C:\test\offline /Get-ScratchSpace</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>/Get-TargetPath</strong></p></td>
<td align="left"><p>Retrieves the target path of the Windows PE image. The target path represents a path to the root of the Windows PE image at boot time. For example:</p>
<p><strong>Dism /image:C:\test\offline /Get-TargetPath</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>/Set-ScratchSpace:</strong><em>&lt;size_of_ScratchSpace&gt;</em></p></td>
<td align="left"><p>Sets the available scratch space, in megabytes. Valid values are 32, 64, 128, 256 and 512. For example:</p>
<p><strong>Dism /image:C:\test\offline /set-ScratchSpace:128</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>/Set-TargetPath :</strong><em>&lt;target_path&gt;</em></p></td>
<td align="left"><p>For hard disk boot scenarios, this option sets the location of the Windows PE image on the disk.</p>
<p>Note the following limitations when setting the target path:</p>
<ul>
<li><p>The path must be at least three characters and no longer than 32 characters</p></li>
<li><p>The path must start with a letter (any letter from C to Z)</p></li>
<li><p>The drive letter must be followed by <em>:</em></p></li>
<li><p>The remainder of the path must not contain any invalid characters, such as Unicode characters</p></li>
<li><p>The path must be absolute, no &quot;.&quot; or &quot;..&quot; elements</p></li>
<li><p>The path must not contain any blank spaces or &quot;&amp;quot;</p></li>
</ul>
<p>For example:</p>
<p><strong>Dism /image:C:\test\offline /Set-TargetPath:X:</strong></p></td>
</tr>
</tbody>
</table>


## <span id="related_topics"></span>Related topics


[Windows PE for Windows 10](winpe-intro.md)

[Wpeutil Command-Line Options](wpeutil-command-line-options.md)

[What is DISM?](what-is-dism.md)

[DISM Image Management Command-Line Options](dism-image-management-command-line-options-s14.md)

[Deployment Image Servicing and Management (DISM) Command-Line Options](deployment-image-servicing-and-management--dism--command-line-options.md)

 

 






