[The standard Ghidra README.md file is here.][readme_orig]

# Projects to extend Ghidra for retrocomputing

- Add a way to redefine the hexadecimal sigil.
  Currently it's always the prefix `0x` but on most platforms in assembly language it was the prefix `$` and on the TI-99/4A for both TMS-9900 and GPL (Graphics Programming Language) it was the prefix `>`.

- Add support for Options in FileSystems similar to what we have for Loaders.
  - Option for including the headers or not.
  - Choice or format for 'wrapping' files that have extra info in the filesystem outside the file but necessary or useful for disassembly.
    - Apple II has a choice of MacBinaryII headers and NAPS filename extensions.
    - Commodore 64 has X00/P00 filename extensions.
    - TI-99/4A has a choice of two 128-byte headers: FIAD (V9T9) ) and TIFILES (XMODEM).

- Add a way for FileSystems to inform the UI about filetypes.
  Currently it depends solely on the file extension.

[The standard Ghidra README.md file is here.][readme_orig]

[readme_orig]: README_orig.md