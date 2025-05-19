# Building a haskell program on arch linux

2025-03-11 17:36:35

I use Arch Linux's package respository for installing haskell.

when trying to build a program I was working on in Haskell, it would fail - telling me that a load of the modules could not be found.

It is something to do with "static linking", but I don't really know what that means at the moment.

My solution was to add the `-dynamic` flag to the build command:

```bash
ghc -dynamic --make programname
```

Update: i'm now using GHCup for haskell installation and building just works for me. Will keep this zet for posterity.
