# Installation

- When we run the Windows installer, it will set the `GSTREAMER_1_0_ROOT_MSVC_X86_64` environment variable to the path of the `gstreamer-1.0` installation.

```
$(VC_IncludePath);$(WindowsSDK_IncludePath);$(GSTREAMER_1_0_ROOT_MSVC_X86_64)include\gstreamer-1.0;$(GSTREAMER_1_0_ROOT_MSVC_X86_64)include\glib-2.0
```

not working

```
  <ImportGroup Label="PropertySheets" Condition="'$(Platform)'=='x64'">
    <Import Project="$(UserRootDir)\Microsoft.Cpp.$(Platform).user.props" Condition="exists('$(UserRootDir)\Microsoft.Cpp.$(Platform).user.props')" Label="LocalAppDataPlatform" />
    <Import Project="$(GSTREAMER_1_0_ROOT_X86_64)\share\vs\2010\libs\gstreamer-1.0.props" Condition="exists('$(GSTREAMER_1_0_ROOT_X86_64)\share\vs\2010\libs\gstreamer-1.0.props')" />
    <Import Project="$(GSTREAMER_1_0_ROOT_X86_64)\share\vs\2010\msvc\x86_64.props" Condition="exists('$(GSTREAMER_1_0_ROOT_X86_64)\share\vs\2010\msvc\x86_64.props')" />
  </ImportGroup>
```

not working

```
<Import Project="$(GSTREAMER_1_0_ROOT_MSVC_X86_64)\share\vs\2010\libs\gstreamer-1.0.props" />
```

working
