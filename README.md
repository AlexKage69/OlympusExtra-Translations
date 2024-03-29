# OlympusExtra-Translations

These are translation packages for OlympusExtra Mod for Hades.

Latest support is 1.3.3.
Dependency on OlympusExtra being installed correctly.

To Run:
Download this repository under Mods/ and un-comment modfile.txt, for example to support french: 

```:: Include "modfile_de.txt"
:: Include "modfile_es.txt"
Include "modfile_fr.txt"
:: Include "modfile_it.txt"
:: Include "modfile_ja.txt"
:: Include "modfile_ko.txt"
:: Include "modfile_pl.txt"
:: Include "modfile_pt-BR.txt"
:: Include "modfile_ru.txt"
:: Include "modfile_zh-CN.txt"
```

Then run modimporter.exe.

To Help with Translation:
I created a automatic process to extract the translation from the game for OlympusExtra. 
Fill free to fill up the BLANKS in the text and add them as new Pull Requests.
DisplayName and Description from english are captionned in comments.

____________________________ OLD EXPLANATION _______________________

If you want to fill it up, all you have to do is search in the OlympusExtra Mod code like Apollo.lua for example.

For file _LootData.pl.sjson, search "LootData", if nothing then nothing.
If you find it, you can extract each ID for new translation.

Example: In Apollo.lua, you'll find in LootData the following.

ApolloWithZeus01 = {
	Name = "ApolloWithZeus01",
	PlayOnce = true,
	PreEventFunctionName = "BoonInteractPresentation", PreEventFunctionArgs = { PickupWait = 1.0, },
	HasTraitNameInRoom = "MasterBoltTrait",
    { Cue = "/VO/Apollo_0041",
		StartSound = "/Leftovers/World Sounds/MapZoomInShort",
		Text = "Seeing you struggle with your father made me realise something, Zagzag. Fathers and sons work much better together. My father and I put together something that might help you." },
	{ Cue = "/VO/Zeus_0250",
		PortraitExitWait = 0.35,
		PreLineFunctionName = "BoonInteractPresentation", PreLineWait = 0.5,
		StartSound = "/SFX/ZeusBoonThunder",
		EndSound = "/Leftovers/World Sounds/MapZoomInShort",
		Speaker = "NPC_Zeus_01", Portrait = "Portrait_Zeus_Default_01",
		Text = "That's right, Nephew! I feel generous and I know you feel grateful. Let's show him our power, young son." },
},

From that you can extract 2 required translation and add them to _LootData.pl.sjson.

{
      /*
        Event: ApolloWithZeus01
        Apollo: Seeing you struggle with your father made me realise something, Zagzag. Fathers and sons work much better together. My father and I put together something that might help you.
        Zeus: That's right, Nephew! I feel generous and I know you feel grateful. Let's show him our power, young son.
      */
      Id = "Apollo_0041"
      Speaker = "Apollo"
      DisplayName = "Polish Text Here"
    }
    {
      /*
        Event: ApolloWithZeus01
        Apollo: Seeing you struggle with your father made me realise something, Zagzag. Fathers and sons work much better together. My father and I put together something that might help you.
        Zeus: That's right, Nephew! I feel generous and I know you feel grateful. Let's show him our power, young son.
      */
      Id = "Zeus_0250"
      Speaker = "Zeus"
      DisplayName = "Polish Text Here"
    }

Comments /* */ are optional, but it's useful for reference.

** Eventually we wanted to have .sjson to be auto generated, but it's not a priority and a late item for us.
