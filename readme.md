<!--
GENERATED FILE - DO NOT EDIT
This file was generated by [MarkdownSnippets](https://github.com/SimonCropp/MarkdownSnippets).
Source File: /readme.source.md
To change this file edit the source file and then run MarkdownSnippets.
-->

# <img src="/src/icon.png" height="30px"> Verify.Xaml

[![Build status](https://ci.appveyor.com/api/projects/status/o2iy3b7k9le0ntps?svg=true)](https://ci.appveyor.com/project/SimonCropp/verify-winforms)
[![NuGet Status](https://img.shields.io/nuget/v/Verify.WinForms.svg)](https://www.nuget.org/packages/Verify.WinForms/)

Extends [Verify](https://github.com/SimonCropp/Verify) to allow verification of WinForms UIs.

Support is available via a [Tidelift Subscription](https://tidelift.com/subscription/pkg/nuget-verify.winforms?utm_source=nuget-verify.winforms&utm_medium=referral&utm_campaign=enterprise).

<!-- toc -->
## Contents

  * [Usage](#usage)
  * [OS specific rendering](#os-specific-rendering)
  * [Security contact information](#security-contact-information)<!-- endtoc -->


## NuGet package

https://nuget.org/packages/Verify.WinForms/


## Usage

Enable VerifyXaml once at assembly load time:

<!-- snippet: Enable -->
<a id='snippet-enable'/></a>
```cs
VerifyWinForms.Enable();
```
<sup><a href='/src/Tests/GlobalSetup.cs#L9-L11' title='File snippet `enable` was extracted from'>snippet source</a> | <a href='#snippet-enable' title='Navigate to start of snippet `enable`'>anchor</a></sup>
<!-- endsnippet -->

A visual element (Form/Control etc) can then be verified as follows:

<!-- snippet: FormUsage -->
<a id='snippet-formusage'/></a>
```cs
[Fact]
public Task FormUsage()
{
    return Verify(new MyForm());
}
```
<sup><a href='/src/Tests/TheTests.cs#L14-L20' title='File snippet `formusage` was extracted from'>snippet source</a> | <a href='#snippet-formusage' title='Navigate to start of snippet `formusage`'>anchor</a></sup>
<!-- endsnippet -->

With the state of the element being rendered as a verified file:

[TheTests.FormUsage.verified.png](/src/Tests/TheTests.FormUsage.verified.png):

<img src="/src/Tests/TheTests.FormUsage.verified.png" width="200px">


## OS specific rendering

The rendering of Form elements can very slightly between different OS versions. This can make verification on different machines (eg CI) problematic. There are several approaches to mitigate this:

 * Using a [custom comparer](https://github.com/SimonCropp/Verify/blob/master/docs/comparer.md)


## Security contact information

To report a security vulnerability, use the [Tidelift security contact](https://tidelift.com/security). Tidelift will coordinate the fix and disclosure.


## Icon

[Gem](https://thenounproject.com/term/gem/2247823/) designed by [Adnen Kadri](https://thenounproject.com/adnen.kadri/) from [The Noun Project](https://thenounproject.com/creativepriyanka).
