---
author: joshbax-msft
title: WHCKProximityTest- UnSubscribe
description: WHCKProximityTest- UnSubscribe
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: f8ed7243-84d1-4bf5-aeeb-1f0cc6d2dfc1
---

# WHCKProximityTest- UnSubscribe


This manual test determines whether a proximity-compliant device handles standard publication and subscription events correctly. The test also verifies that the driver deletes subscription messages when the subscription handle is closed.

To successfully complete this test, you must respond to prompts that appear during the test.

## Test details


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Associated requirements</strong></p></td>
<td><p>Device.BusController.NearFieldProximity.ProviderImplementation</p>
<p>[See the device hardware requirements.](http://go.microsoft.com/fwlink/p/?linkid=254483)</p></td>
</tr>
<tr class="even">
<td><p><strong>Platforms</strong></p></td>
<td><p>Windows RT (ARM-based) Windows 8 (x64) Windows 8 (x86) Windows RT 8.1 Windows 8.1 x64 Windows 8.1 x86</p></td>
</tr>
<tr class="odd">
<td><p><strong>Expected run time</strong></p></td>
<td><p>~2 minutes</p></td>
</tr>
<tr class="even">
<td><p><strong>Categories</strong></p></td>
<td><p>Certification Functional</p></td>
</tr>
<tr class="odd">
<td><p><strong>Type</strong></p></td>
<td><p>Manual</p></td>
</tr>
</tbody>
</table>

 

## Running the test


Before you run the test, complete the test setup as described in [Proximity Controller Testing Prerequisites](proximity-controller-testing-prerequisites.md).

## Troubleshooting


For troubleshooting information, see [Troubleshooting Bus Controller Testing](troubleshooting-bus-controller-testing.md).

## More information


This test is run by using two test computers. Computer A runs the WHCKNearFieldInitiator.dll file and grades the test as Pass or Fail. Computer B runs the WHCKNearFieldResponder.dll file and returns a Pass or Fail result only to report on the computer’s support operations to the test.

Computer A subscribes to and then waits for Computer B’s publication. Computer A during the wait closes the subscription handle. Computer A expects to reach a timeout on waiting for the subscription to be fulfilled. Computer B makes a publication. Computer B then subscribes to the DeviceDeparted event and waits for this event to occur.

### Command syntax

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Command option</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Te.exe /inproc WHCKNearFieldInitiator.dll /name:&quot;CWHCKProximityTestInitiator::UnSubscribe&quot;</strong></p></td>
<td><p>Runs the test.</p></td>
</tr>
</tbody>
</table>

 

**Note**  
For command-line help for this test binary, type the following:

**Te.exe /inproc WHCKNearFieldInitiator.dll /name:”CWHCKProximityTestInitiator::UnSubscribe” /listproperties**.

 

### File list

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>File</th>
<th>Location</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>NotifyAttention.png</p></td>
<td><p>&lt;testbinroot&gt;\dtmtest\NearField</p></td>
</tr>
<tr class="even">
<td><p>NotifyPrepare.png</p></td>
<td><p>&lt;testbinroot&gt;\dtmtest\NearField</p></td>
</tr>
<tr class="odd">
<td><p>NotifyProximate.png</p></td>
<td><p>&lt;testbinroot&gt;\dtmtest\NearField</p></td>
</tr>
<tr class="even">
<td><p>NotifyRemove.png</p></td>
<td><p>&lt;testbinroot&gt;\dtmtest\NearField</p></td>
</tr>
<tr class="odd">
<td><p>Te.exe</p></td>
<td><p>&lt;TAEFBinRoot&gt;</p></td>
</tr>
<tr class="even">
<td><p>WHCKNearFieldInitiator.dll</p></td>
<td><p>&lt;testbinroot&gt;\dtmtest\NearField</p></td>
</tr>
<tr class="odd">
<td><p>WHCKNearFieldResponder.dll</p></td>
<td><p>&lt;testbinroot&gt;\dtmtest\NearField \</p></td>
</tr>
</tbody>
</table>

 

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bp_hck\p_hck%5D:%20WHCKProximityTest-%20UnSubscribe%20%20RELEASE:%20%284/27/2016%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")



