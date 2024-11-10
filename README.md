[The standard Ghidra README.md file is here.][readme_orig]

---

# Projects to extend Ghidra for retrocomputing

- Add a way to redefine the hexadecimal sigil.  
  Currently it's always the prefix `0x` but on most platforms in assembly language it was the prefix `$` and the TI-99/4A used the prefix `>`.
  - Discussion: [6992][d6992]
  - Source: [Scalar.java][scalar_java]

- Add support for Options in FileSystems similar to what we have for Loaders.
  - Option for including the headers or not.
    - This is probably better handled in each individual Loader. But see the following bullet point.
  - Choice of format for 'wrapping' files that have extra info in the filesystem outside the file but necessary or useful for disassembly.
    - Apple II has a choice of MacBinaryII headers and NAPS filename extensions.
    - Commodore 64 has X00/P00 filename extensions.
    - TI-99/4A has a choice of two 128-byte headers: FIAD (V9T9) and TIFILES (XMODEM).

- Add a way for FileSystems to inform the UI about filetypes.  
  Currently it depends solely on the file extension. But many filesystems have filetype info in the binary structure.
  - Discussion: [6953][d6953]
  - Pull request: [7062][pr7062]
 
- Add support for A-line and F-line traps, used in various ways, by Motorola 680x0 platforms.
  - March 2019 issue: [140][i140]
  - April 2019 issue: [487][i487]
  - Pull request: [7126][pr7126]

  ---

[The standard Ghidra README.md file is here.][readme_orig]

[d6953]: https://github.com/NationalSecurityAgency/ghidra/discussions/6953
[d6992]: https://github.com/NationalSecurityAgency/ghidra/discussions/6992
[pr7062]: https://github.com/NationalSecurityAgency/ghidra/pull/7062
[pr7126]: https://github.com/NationalSecurityAgency/ghidra/pull/7126
[i140]: https://github.com/NationalSecurityAgency/ghidra/issues/140
[i487]: https://github.com/NationalSecurityAgency/ghidra/issues/487
[readme_orig]: README_orig.md
[scalar_java]: https://github.com/hippietrail/ghidra/blob/master/Ghidra/Framework/SoftwareModeling/src/main/java/ghidra/program/model/scalar/Scalar.java#L286
