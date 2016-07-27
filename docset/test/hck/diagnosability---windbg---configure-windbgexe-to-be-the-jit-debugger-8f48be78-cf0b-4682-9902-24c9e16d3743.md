---
author: joshbax-msft
title: Diagnosability - WinDbg - Configure WinDbg.exe to be the JIT debugger
description: Diagnosability - WinDbg - Configure WinDbg.exe to be the JIT debugger
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: b18f68b3-8d44-4391-9136-8b43a96982f9
---

# Diagnosability - WinDbg - Configure WinDbg.exe to be the JIT debugger


This optional test is provided to help troubleshoot certain test failures and is not required for certification.

You can use this optional test to configure WinDbg.exe to be the default Just-In-Time debugger. This causes test applications to break into the debugger when they crash, to allow additional debugging. For more information, see [Enabling Postmortem Debugging](http://go.microsoft.com/fwlink/p/?linkid=303793).

## Test details


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Associated requirements</strong></p></td>
<td><p>Device.DevFund.Reliability.Discretional System.Fundamentals.Reliability.Discretional</p>
<p>[See the system hardware requirements.](http://go.microsoft.com/fwlink/p/?linkid=254482)</p></td>
</tr>
<tr class="even">
<td><p><strong>Platforms</strong></p></td>
<td><p>Windows 7 (x64) Windows 7 (x86) Windows RT (ARM-based) Windows 8 (x64) Windows 8 (x86) Windows Server 2012 (x64) Windows Server 2008 R2 (x64) Windows RT 8.1 Windows 8.1 x64 Windows 8.1 x86 Windows Server 2012 R2</p></td>
</tr>
<tr class="odd">
<td><p><strong>Expected run time</strong></p></td>
<td><p>~5 minutes</p></td>
</tr>
<tr class="even">
<td><p><strong>Categories</strong></p></td>
<td><p>Optional</p></td>
</tr>
<tr class="odd">
<td><p><strong>Type</strong></p></td>
<td><p>Automated</p></td>
</tr>
</tbody>
</table>

 

## Running the test


You must run the [Diagnosability - Install Jobs - Install Debugging Tools For Windows](diagnosability---install-jobs---install-debugging-tools-for-windows-105e9d96-28ef-418d-9836-d0ca529029d0.md) test, which installs WinDbg.exe on the Windows Hardware Certification Kit (Windows HCK) test system, before you run this test.

## Related topics


[Diagnosability - Just-In-Time Debugging](diagnosability---just-in-time-debugging.md)

 

 






