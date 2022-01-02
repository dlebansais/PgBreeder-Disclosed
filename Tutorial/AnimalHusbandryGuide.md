# Animal Husbandry Guide

[Animal Husbandry](http://wiki.projectgorgon.com/wiki/Animal_Husbandry) (AHu) is a subskill of [Animal Handling](http://wiki.projectgorgon.com/wiki/Animal_Handling) (AH) in Project: Gorgon. This guide aims at giving the reader an overview of the Husbandry skill, and some advice regarding breeding strategies.

## Overview of breeding

Players using Animal Handling need a pet. Pets can be tamed in the wild, bought from other players in the form of caged bred pets (more about that later), or created from existing pets using Animal Husbandry.

A player keeps their pets in their stable, in slots. The process for creating a new pet from existing ones using AHU is fairly straightforward. At one of the stables that allow it ([Leah Bowman](http://wiki.projectgorgon.com/wiki/Leah_Bowman) in Povus or [Arianna Fangblade](http://wiki.projectgorgon.com/wiki/Arianna_Fangblade) in Red Wing Casino), and after making sure one of the stable slot is empty, select the "Husbandry" menu. Then, follow the process of:

+ Selecting a male pet.
+ Selecting a female pet that can be paired with the previously selected male (different species can't pair most of the time, but for instance bees and wasps can). 
+ Confirm the mating.

Once started the empty slot is reserved for mating, which takes a few hours, and if successful is reserved for the incoming baby pet. This last step can takes days, during which the female partner is "pregnant" and cannot be used for AH or other breeding attempts, while the male just need a few hours to recover.

Note that it means the same male can be used for several almost-simultaneous breeding attempts with different females, a distinction that matters when maintaining a livestock of pets of different sex.

After pregnancy has ended, the slot that was holding an "unborn" pet contains the new baby, immediately available for combat or more breeding.

A baby pet is named based on its specie and the total number of pets born for the character. For instance, the 4th born pet, if a Fairy Bee, will be called "Baby Fairy Bee 4". This is helpful when breeding many pets. The name can be changed of course.

### Caged pets

Pets in a stable can be put in cages by obtaining one of the various versions of that item (ex: [Simple Travel Cage](http://wiki.projectgorgon.com/wiki/Simple_Travel_Cage)), then clicking the "Use Item" button for the selected pet, and dragging the cage in the item selection box. This creates a caged pet item that can be traded or sold. Note that all versions of caged pets exist only for a limited time, and you need to make sure the trade takes place before the item vanishes, or the pet is lost forever.

To use a caged pet, simply right-click that item (with an empty slot available to receive it) and the pet is transferred to your stable.

## Overview of genetics

Breeding can take place without being concerned with genetics, but with the help of one of the genetics skills it is possible to create improved pets. The idea is simply that each pet has an associated set of genes, and by combining specific pets, with some luck, the resulting baby is an improved version of their parents.

Improved, in this context, means several things :

+ Genes control the aspect of pets, which means that it is possible to select offspring for the purpose of, for instance, obtaining new pets with the desired color, or shape.
+ Genes also control pet "traits", how powerful they are (see [The Traits of a Pet](http://wiki.projectgorgon.com/wiki/The_Traits_of_a_Pet) for the meaning of each trait). Combining pets with different trait values result in offspring that have sometimes better, and sometimes worse, traits. Knowing how genes are combined helps to predict the result of breeding, toward improved pets.

In the remaining of this guide, we will focus on traits, because they are easier to reason about.

### The gene window

Each pet's genes can be inspected by clicking on the "Genes" button of the selected pet (at a stable that allows breeding, see above). The result is a window similar to these:

![Gene Window with low level in skill](/Tutorial/LowLevelGeneWindow.png?raw=true "Gene Window with low level in skill")

![Gene Window with max level in skill](/Tutorial/MaxLevelGeneWindow.png?raw=true "Gene Window with max level in skill")

The top image shows the gene window with a somewhat low level in the Arthropod Genetics skill, and the bottom image the gene window when that skill is maxed. The difference is obvious, as question marks hide the true "value" of genes when the skill is low. It demonstrates that one can do proper breeding (for the purpose of improving pets, of course) only with a pretty high level in the genetics skill.

Each gene, for a given pet, can have one of 3 "values":

+ Dominant, a filled circle
+ Recessive, an empty circle
+ Mixed, a small filled circle within a bigger empty one.

In the gene window, if one hovers with the mouse over one of the circles, the gene role is revealed.

![Gene role](/Tutorial/GeneRole.png?raw=true "Gene role")

Each gene has two roles:

+ Appearance: the gene adds, or subtracts, a number to a counter associated to the appearance. For example, for "Antenna Scale" that would be the size of the antenna. This guide does not elaborate on that.
+ Trait: the gene also adds, or subtracts, a number to one of the pet traits. In the exemple above, since the gene value is dominant (a filled circle), the gene number is subtracted and this result in a worse pet than if the gene value was recessive. Because, in that case, the gene number would not be subtracted.

(Note that a gene with mixed value acts the same as if it had dominant value. In the rest of this guide, we will ignore the distinction.)

Some genes subtract a number if dominant, others add a number if recessive. Overall, a recessive gene value therefore always result in an increase in the associated trait, and a dominant gene always a decrease.
 
Gene values vary from pets to pets, but roles don't change. The goal then, at least to increase pet traits, is to make sure that no number is subtracted, and that all numbers that could be added are, and consequently, to have all genes (or at least as many as possible) associated to a trait to have a recessive value.

### Combining genes

To obtain recessive values one need to understand how genes are combined. With two parents, for each gene there are 3 x 3 = 9 possibilities, summarized in the table below:

|           | Dominant                  | Mixed                                     | Recessive                   |
| --------- | ------------------------- | ----------------------------------------- | --------------------------- |  
| Dominant  | Dominant: 100%            | Dominant: 50%, Mixed: 50%                 | Mixed: 100%                 |
| Mixed     | Dominant: 50%, Mixed: 50% | Dominant: 25%, Mixed: 50%, Recessive: 25% | Recessive: 50%, Mixed: 50%  |
| Recessive | Mixed: 100%               | Recessive: 50%, Mixed: 50%                | Recessive: 100%             |

Percentages represent the probability of a combination result. For instance, combining a dominant and a mixed gene has half/half chance to result in a dominant or mixed value.

Therefore:

+ If both parents have a dominant value for a given gene, the baby pet will also have a dominant value. The associated trait cannot be improved that way.
+ If both parents have a recessive value for a given gene, the baby pet will also have a recessive value. The value of this gene is of no concern, it is "safe".
+ If parents have a different value then some luck is involved. The process of selection consists in releasing pets with bad gene values and keeping pets with good gene values, then breeding again, until all parents have recessive values in genes of interest.

### Gene rarity

Looking back at the gene window, with max skill level in genetics, you'll notice that the line labeled "07" (we will call it chromosome 7 from now on) only has genes with dominant values. This is not a coincidence. Almost always, all genes for that chromosome are dominant, and rarely one of them, even more rarely two, are not.

This means that in practice the number for all genes of chromosome 7 is always, or almost always, subtracted from the trait.

This is a key issue: because the genome of parents has genes that are almost always dominant, the total of added and subtracted numbers for traits is inherently limited.

## Monster genes

If players could use their own pets and no others, genes dominant for all pets in the stable would be impossible to improve. As a matter of fact, players cannot exchange breeding pets: a caged pet is always turned to neutral genre, and cannot participate to breeding. Trading with other players is not the solution.

However, there is another source of new pets: tamed monsters. Taming sends a captured pet to the stable, and it can then immediately start mating.

To help finding a monster with desired gene values, at level 50 in the corresponding genetics skill players acquire the "Analyze Genes" sidebar ability. Using it on a live mob shows a gene window similar to that of stable pets. Note, however, that the ability takes five seconds to channel, and is interrupted by attacks. For this reason, you typically want some help, or a mean to keep the target mesmerized while analyzing its genes.

If a target is found with good genes, it can be immediately tamed.

Also note that it is possible to analyze dead creatures, but obviously it's too late to tame them. That fact, however, can be useful when deciding of a breeding strategy, as we are going to see.  

## Breeding strategy

This section offers advices for selecting which combination of parents to breed and how to proceed to eventually obtain pets with high traits.

### Calculating gene numbers

The game doesn't tell you what a gene number is, other than its sign. For instance we saw before that the tooltip for the 17th gene of chromosome 7 is "Friendliness-". So we know a dominant gene decreases friendliness, but how much?

This number is the same for everyone, so you can just ask other players to share what they discovered. But they of course had to figure it out themselves at some point. So, how to proceed? Here is the general idea: if two pets have close enough gene values in such a way that there is only one gene that affects friendliness that has a different value (one pet has it recessive, the other not) then the difference is immediately obtained by subtracting their friendliness.

To make it concrete by example, say "Baby Fairy Bee 1" has the 17th gene of chromosome 7 dominant (or mixed, it's the same), while "Baby Fairy Bee 2" has it recessive. If "Baby Fairy Bee 1" has friendliness 45 and "Baby Fairy Bee 2" friendliness 52 then the gene number is 45 - 52 = -7.

Once a gene number is known, pets can differ by that gene and one other, for friendliness, and by taking into account this difference of -7 we can calculate the number for that other gene. And then repeat the process until all numbers are known.

This is similar to solving a system of linear equations, and in the case of traits there are between 20 and 23 unknowns, depending on the trait.

### Achievable traits

Consider a livestock of pets, and assume we managed to breed them to obtain the most optimized baby. A baby for which, if there existed a non-dominant value for a given gene, we managed through breeding to give it a recessive value. This is the maximum number we can hope to obtain for all traits.

Hard numbers are not known at this stage of the game, but if one ignores rare genes (and there won't be many of them in the livestock when a player begins AHu), assuming all rare genes have dominant values, then the maximum one can expect for a trait is approximately 75 on average.

Specifically, even with perfect breeding, unconstrained by time and money, the best pet one can achieve will have traits around 75 on average. This when we know traits can go above 100 (though values above 100 have no effect).

Therefore, to obtain a maxed out baby, one must tame pets with rare genes and breed them with the rest to introduce non-dominant values for rare genes and increase the potential of their livestock.

### Constraints

When planning breeding in the long term, there are several things to consider:

+ There is a maximum number of breeding attempts, which translates in a hard limit on how fast you can reach your goal. Expect 4 or 5 simultaneous breeding attempts at most.
+ You can buy stable slots, but again there is a maximum and most players will not have a livestock bigger than 20 pets.
+ Breeding costs money, and if you want to speed it, resources, though it's not a big issue if you're focusing on this feature of the game.
+ About half of your livestock will be male, and the other half female, but be careful not to have too many males. Remember that males don't stay pregnant and can participate to new breeding attempts more quickly than females. This said, you still need to maintain good values for genes on both males and females, which divides your number of slots by half.
+ You might want to breed more than one specie. For instance, if you focus on bees only, then your entire stable can be dedicated to bee pets. But if you want to have say maxed out bees and wasps in the end, you need to be careful: when mating a bee and a wasp, the chance of obtaining either is based on intelligence. If your livestock of bees (for instance) outgrows wasps by intelligence, or worse if you plan to introduce wild wasps only at the end, babies will almost always be bees and it might prove very difficult to create a maxed out wasp.
+ This is even worse when breeding species that cannot mix, like bees/wasps and cats.

For these reasons, it is important to decide for a strategy that can work in a slot-constrained environment. This guide suggests a strict minimum of 6 slots per specie, and leave it to you to increase the number of slots at the expense of breeding less species.

### Why focus only on rare genes

This guide suggests to completely ignore genes that are not rare, and to focus only on obtaining recessive values for rare genes. Why?

First of all, let's consider what would happen if pets were combined at random. If we return to the table in the [Combining genes](#combining-genes) section, we see that probabilities of mixing between dominant, mixed and recessive values are evenly distributed. The result should also be random. But, in fact, it is not. This is because there is a probability, albeit small, that all values become either all dominant or all recessive. And when this happens, there is no way back, the gene value is stuck. Therefore, when combining pets at random, over time there are less and less mixed genes until they vanish. Babies then are exactly equal to their parents and nothing changes.

Second of all, when taming a wild mob there is no way to predict what will be the distribution of dominant, mixed and recessive genes for common genes. All previous efforts to obtain only recessive values of a given gene could have been wasted if the last tamed pets all have recessive values of that gene. Breeding would then naturally give overwhelming odds of getting good mixing results with no special effort.

Therefore, it is better to focus on rare genes, for which we already know they will be dominant on new pets. Other genes will eventually reach either recessive or dominant value, and there is no way to predict if that's good or bad.

### How to determine rarity

We have seen that all genes in chromosome 7 are rare (though no proof was given). How can we know which gene is rare and which is not?

The idea is to analyze a lot, and with the help of statistics find rare genes by deciding of a threshold (say, 5%) then counting how often a gene has recessive value, and label "rare" those genes whose count is below the threshold.

As a reminder, it is possible to analyze genes of a dead creature. Hence to determine rarity just kill and analyze a lot of monsters, until you have convincing statistics.

On a side note, rarity is the same for all players. This is typically a work that can be shared.

### Breeding with 6 slots

Here we are going to work with 6 slots, starting with one male and one female, both with identical gene values. Since we're only considering rare genes, it can even be all-dominant initially, but quickly there will be at least one recessive gene for both the male and the female.

More specifically, we start like this:

```
1- M: RD...DD
2- F: RD...DD
```

Where 1 and 2 are the first two slots in the stable, M means male and F female, and D, R (and below, x) indicate dominant or recessive values (and mixed) respectively.

Say we capture a new pet with the following gene values:

```
3- ?: DD...DR
```

? means the sex can be anything. When you inspect a live creature you can see their sex, but in our case it doesn't matter since we have both a male and female with identical gene values. A captured male would speed up the process but usually once you spot a good pet to tame you don't want to ignore it just because it has the wrong sex. Hence why we want both a male and female in the stable to start with.

Sticking to our example, say the captured pet is a male. We then breed it with the female and then the stable looks like this:

```
1- M: RD...DD
2- F: RD...DD
3- M: DD...DR
4- ?: xD...Dx
```

The first baby can be either male or female, but different genes are necessarily mixed (see the mixing table: R and D always result in x)

Notice that gene other than first and last are all dominant. They will obviously stay that way all the time and we can ignore them.

The idea is now to breed pets with mixed genes with their parents:

```
1- M: RD...DD
2- F: RD...DD
3- M: DD...DR
4- ?: xD...Dx
5- ?: ?D...D?
6- ?: ?D...D?
```

There are more question marks now, because the result is probabilistic. However, we can just release babies that ended up with undesired values and retry until we get something good. For instance (look at slot 6):

```
1- M: RD...DD
2- F: RD...DD
3- M: DD...DR
4- ?: xD...Dx
5- ?: ?D...D?
6- M: xD...DR
```

This combination of getting a male with the first gene mixed and the last gene recessive had 1 chance out of 8 to occur, but now we can replace the pet in slot 3 with that one from slot 6:

```
1- M: RD...DD
2- F: RD...DD
3- M: xD...DR
```

Then breed 3 and 2, with 50% chance to obtain the first gene as recessive:

```
1- M: RD...DD
2- F: RD...DD
3- M: xD...DR
6- ?: RD...DR
```

And now we got one baby that is better than either the male or the female we started with. Say it's a female, this gives us:

```
1- M: RD...DD
2- F: RD...DR
3- M: xD...DR
```

The new gene is now in the stable in the form of a good female. We can repeat the process until we get a male, and then get rid of all extra intermediate pets we no longer need. This gives us at the end:

```
1- M: RD...DR
2- F: RD...DR
```

Reorganizing genes by moving the last to second position (since all of this is completely a matter of convention).

```
1- M: RRD...D
2- F: RRD...D
```

And we repeat the process again and again.

The reason we need 6 slots is not immediately apparent, because in the simple example above we didn't make use of all 6. Let's consider the more general case below:

```
1- M: R...RD
2- F: R...RD
3- M: DD..DR
```

First two pets are the result of previous breeding. The third pet only has one recessive gene (but that's the one we wanted). We can, counting on half/half male/female and in a non-optimal way releasing all extra, breed until we get:

```
1- M: R...RD
2- F: R...RD
3- M: DD..DR
4- M: xx..xx
5- F: xx..xx
```

That is, obtain one male and one female with all mixed genes.

Then we breed slots 3 & 5: 

```
1- M: R...RD
2- F: R...RD
3- M: DD..DR
4- M: xx..xx
5- F: xx..xx
6- ?: ??..??
```

Nothing then is guaranteed, however there is a 50% chance the last gene is recessive, which gives:

```
1- M: R...RD
2- F: R...RD
3- M: DD..DR
4- M: xx..xx
5- F: xx..xx
6- ?: ??..?R
```
We can then replace slot 3 with slot 6 because it is better. At worse, other genes have dominant values but on average half of them are already mixed.

We then breed 3 with 4 or 5, based on sex, and relentlessly eliminate offspring that have unfavorable values until 1 and 2 are eventually replaced. And then we tame a new pet, and repeat the process.
