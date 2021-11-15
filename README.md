# Download
The latest version (1.0.0.6) is [here](https://github.com/dlebansais/PgBreeder-Disclosed/releases/download/v1.0.0.6/PgBreeder.exe) with updated [release notes](https://github.com/dlebansais/PgBreeder-Disclosed/blob/master/ReleaseNotes.md).

# PgBreeder
This application helps players of Project: Gorgon (aka PG) to manage pets they breed with the Animal Husbandry skill. With PgBreeder you can:

+ Record info about pets like their parents, sex, stats and genes.
+ Capture genes from the game window quickly.
+ Obtain a summary of the quality of your pool of genes.
+ Save information about each genes when you have figure them out.
+ Exchange genome information between players with Export & Import.  

*Information about pets is saved in text files, I strongly recommend to archive them regularly. I also recommend to regularly export genome to a text file*. 

# User Manual

When you start PgBreeder for the first time, it looks like this:

![Main application window](/Screenshots/main_window.png?raw=true "The main application window")

## Managing pets

Add a new pet with the **New Pet** button, then click **Capture**. This will open the gene scanner window (see below how to set it up). Once you have captured genes, and updated info about your pet, it will be automatically saved in you pet folder upon exit.

You can change the pet folder to somewhere more convenient than the folder where PgBreeder.exe was copied to (in particular, using `C:\Program Files` doesn't work well). However, when you change it you'll need to copy pet files manually and restart the application.

### Stable

Not all your pets can be in stables, and often you must release them or move them to cages. There is a checkbox to indicate that a pet is in stables and available for breeding. These pets are displayed in **bold**.

If a pet is pregant, or mating, it still cannot be used for breeding but that's temporary. The corresponding checkbox let you specify that. It is unchecked every time the application is restarted.

### Pets tab

This tab displays the genome of the currently selected pet. Double-click a gene to change how it modifies traits (if applicable). Once done, you can export this information in a text file with the **Genome** button. Conversely, you can import what others have found and this new information will appear in tooltips.

The *best pairing mate* is a suggestion, based on genes of pets of the opposite sex that are in stables and not busy, of the best pet to mate with for the purpose of obtaining recessive genes. Three calculations are made:

+ A generic score, where a resulting mixed gene counts for 1/2 and a recessive gene for 1.
+ A recessive score, where only recessive resulting genes count (useful when optimizing a pool).
+ A traits score, where each gene count based on its effect on traits (useful when breeding for optimized battlefield traits). All traits are considered of equal value for now, except that Virility/Fertility doesn't count.

## Pool

This tab displays for each gene how easy it is to obtain new pets with recessive genes. It uses a combination of shape and color.

+ Red and dominant: none of your pets have any mixed or recessive version of this gene. New pets will always have it dominant.
+ Red and mixed: at least one of your pet has this gene in mixed form. It can give birth to a new pet with this gene mixed as well, and with opposite sex. Mating them has then 25% chance to give a recessive version. For this reason, this pool quality is called "second generation".
+ Green and mixed: this gene is present as recessive in one of your pet, but not twice in pets of opposed sex. It always has a probability to end up mixed or dominant in offsprings. This is called a "first generation" gene.
+ Green and recessive: this gene is present as recessive in at least two pets of opposed sex. Mating them will always result in a recessive version of the gene. 

Note that you can filter genes that modify pet traits, if that's what you're interested in.

## Stats

The *Stats* tab shows:

+ How genes where mixed when two pets gave an offspring. It should indicate any deviation from the average over time (if there is any).
+ How many genes you have figured out (see above) and how many you still don't know.

## Scanning genes

The interface of the gene scanner is similar to that found in [PgSurveyor](https://github.com/dlebansais/PgSurveyor-Disclosed/blob/master/README.md), although it works in the opposite way: it captures what's on the screen.

![Scanner window](/Screenshots/scanner_window.png?raw=true "The scanner window")

+ Drag the top-left and bottom-right corner of the scanner border to align them with the gene window in the game. The border around the map window should adjust exactly around the top, left, right and bottom gene circles. The screenshot above shows a scanner ready to capture.
+ Click the scan button (bottom-right) to capture genes. These will appear as overlays over the game, but slightly transparent, and you can quickly check that they were all captured properly. If they weren't, ajust borders and try again until you find a setting that works. The position of each corners will be saved when you return to the application (button at the bottom-left). 
+ Fill other info about the pet that you know, and don't forget to give it a name!

### New gene discovery

If you capture genes of a **live** pet in the wild (or, for that matter, a lucky newborn pet), genes that improve your pool appear in *orange*. Genes that don't appear in *green*.

# Certification

This program is digitally signed with a [CAcert](https://www.cacert.org/) certificate.
