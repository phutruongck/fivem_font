[FiveM Font]
Convert TTF Font to GFX Font
Step 0: Create a XML file from your font, follow the code

<?xml version="1.0" encoding="iso-8859-1" ?>

<movie version="8" width="320" height="240" framerate="12">
  <frame>
    <library>
      <font id="Fira Sans" import="fs.ttf" name="Fira Sans"/>
    </library>
  </frame>
</movie>

Step 1: Convert TTF to SWF by SWFMILL, follow the command
swfmill simple quicksand.xml quicksand.swf
then copy quicksand.swf to GFxExport folder to next step
Step 2: Convert SWF to GFX by GFxExport, follow the command
gfxexport quicksand.swf

==> Done, you have a gfx font

How to use GFX Font

Important: Store font file to stream folder

RegisterFontFile('font file')
fontId = RegisterFontId('font id')
SetTextFont(fontId)