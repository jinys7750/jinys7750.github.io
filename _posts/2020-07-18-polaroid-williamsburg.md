---
layout: post
title: "Polaroid Williamsburg"
date: 2020-07-18
description: 
image: /assets/images/placeholder-9.jpg
author: Thomas Vaeth
published: true
tags: 
  - Dummy Text
  - Moon Drinking
  - Kale
---
Etsy squid occupy pop-up. Polaroid +1 everyday carry, kogi chillwave tacos raclette heirloom etsy next level cred locavore. Blog street art DIY, pug crucifix asymmetrical chicharrones. Small batch af single-origin coffee, scenester humblebrag fashion axe viral schlitz you probably haven’t heard of them. Kickstarter synth poutine brunch hoodie. Gochujang marfa raclette kickstarter tumeric kinfolk gentrify retro skateboard, forage meggings polaroid kombucha. Tilde mlkshk fam meggings.

* Actually YOLO marfa tofu shabby chic snackwave. Mumblecore hammock glossier affogato live-edge, tumblr pour-over iceland. Green juice art party flannel meggings, aesthetic kogi actually ramps ugh.
* Church-key crucifix messenger bag health goth
* Try-hard artisan direct trade
* Cold-pressed selfies

1. Actually YOLO marfa tofu shabby chic snackwave. Mumblecore hammock glossier affogato live-edge, tumblr pour-over iceland. Green juice art party flannel meggings, aesthetic kogi actually ramps ugh.
2. Church-key crucifix messenger bag health goth
3. Try-hard artisan direct trade
4. Cold-pressed selfies

### Subway tile
Knausgaard readymade williamsburg tote bag taxidermy, DIY meditation copper mug. Farm-to-table [street art][#] fixie, chambray vice literally four loko vaporware. Pickled taxidermy freegan, affogato pinterest sriracha vexillologist narwhal pour-over. Man braid food truck celiac +1 bicycle rights, semiotics kogi fixie biodiesel woke raw denim quinoa ugh selfies williamsburg. Sartorial af ennui bitters knausgaard, leggings kickstarter slow-carb chia sustainable hexagon. Prism 3 wolf moon occupy ramps wayfarers tumblr narwhal 90’s. Woke chambray church-key before they sold out, gochujang fashion axe franzen banh mi pinterest forage kinfolk.

```java
/**
 * A class to provide a simple list of integers.
 * List resizes automatically. Used to illustrate 
 * various design and implementation details of 
 * a class in Java.
 * 
 * Version 1 only contains the instance variables and
 * the constructors
 * @author scottm
 *
 */
public class IntListVer2{
    // class constant for default size
    private static final int DEFAULT_CAP = 10;
    
    //instance variables
    // iValues store the elements of the list and 
    // may have extra capacity
    private int[] iValues;
    private int iSize;
    
    /**
     * Default add method. Add x to the end of this IntList.
     * Size of the list goes up by 1.
     * @param x The value to add to the end of this list.
     */
    public void add(int x){
        // is there extra capacity available?
        // if not, resize
        if(iSize == iValues.length)
            resize();
        assert 0 <= iSize && iSize < iValues.length;
        iValues[iSize] = x;
        iSize++;
    }
    
    // resize internal storage container by a factor of 2
    private void resize() {
        int[] temp = new int[iValues.length * 2];
        System.arraycopy(iValues, 0, temp, 0, iValues.length);
        iValues = temp;
    }
    
    /**
     * Return a String version of this list. Size and 
     * elements included.
     */
    public String toString(){
        // we could make this more effecient by using a StringBuffer.
        // See alternative version
        String result = "size: " + iSize + ", elements: [";
        for(int i = 0; i < iSize - 1; i++)
            result += iValues[i] + ", ";
        if(iSize > 0 )
            result += iValues[iSize - 1];
        result += "]";
        return result;
    }
    
    // Would not really have this and toString available
    // both included just for testing
    public String toStringUsingStringBuffer(){
        StringBuffer result = new StringBuffer();
        result.append( "size: " );
        result.append( iSize );
        result.append(", elements: [");
        for(int i = 0; i < iSize - 1; i++){
            result.append(iValues[i]);
            result.append(", ");
        }
        if( iSize > 0 )
            result.append(iValues[iSize - 1]);
        result.append("]");
        return result.toString();
    }

    /**
     * Default constructor. Creates an empty list.
     */
    public IntListVer2(){
        //redirect to single int constructor
        this(DEFAULT_CAP);
        //other statments could go here.
    }

    /**
     * Constructor to allow user of class to specify 
     * initial capacity in case they intend to add a lot
     * of elements to new list. Creates an empty list.
     * @param initialCap > 0
     */    
    public IntListVer2(int initialCap) {
        assert initialCap > 0 : "Violation of precondition. IntListVer1(int initialCap):"
            + "initialCap must be greater than 0. Value of initialCap: " + initialCap;
        iValues = new int[initialCap];
        iSize = 0;
    }
    
   /**
    * Return true if this IntList is equal to other.<br>
    * pre: none
    * @param other The object to comapre to this
    * @return true if other is a non null, IntList object
    * that is the same size as this IntList and has the
    * same elements in the same order, false otherwise.
    */
    public boolean equals(Object other){
        boolean result;
        if(other == null)
            // we know this is not null so can't be equal
            result = false;
        else if(this == other)
            // quick check if this and other refer to same IntList object
            result = true;
        else if( this.getClass() != other.getClass() )
            // other is not an IntList they can't be equal
            result = false;
        else{
            // other ris not null and refers to an IntList
            IntListVer2 otherIntList = (IntListVer2)other;
            result = this.iSize == otherIntList.iSize;
            int i = 0;
            while(i < iSize && result){
                result = this.iValues[i] == otherIntList.iValues[i];
                i++;
            }
        }
        return result;     
    }

}
```

![Placeholder](/assets/images/placeholder-2.jpg)

Meh food truck tofu succulents, literally waistcoat skateboard poke pop-up cold-pressed put a bird on it cliche umami cornhole kale chips. Man braid 8-bit irony selvage, butcher blog everyday carry. Af meggings tacos ugh la croix skateboard. Biodiesel paleo prism kombucha seitan drinking vinegar. Single-origin coffee lo-fi cardigan, poutine roof party bitters taxidermy post-ironic umami vaporware. Austin edison bulb leggings cliche. Literally church-key umami, vegan irony art party vinyl edison bulb selfies lumbersexual deep v fingerstache flexitarian.

> Sartorial af ennui bitters knausgaard, leggings kickstarter slow-carb chia sustainable hexagon. Prism 3 wolf moon occupy ramps wayfarers tumblr narwhal 90's.
> <cite>Man braid</cite>

#### Subway tile
Slow-carb cornhole crucifix thundercats intelligentsia. Trust fund bushwick la croix, 8-bit hell of ennui chicharrones vegan master cleanse tilde subway tile bespoke roof party. Next level celiac bushwick coloring book subway tile. Lyft knausgaard four loko, twee sustainable narwhal letterpress PBR&amp;B kombucha paleo mixtape helvetica. Photo booth gastropub yr sartorial kitsch godard, etsy hella literally kale chips. Mixtape hella readymade selvage taxidermy cornhole umami four dollar toast, yr seitan blog. Butcher whatever copper mug, keffiyeh authentic humblebrag irony distillery williamsburg fingerstache helvetica keytar glossier.

Gluten-free la croix activated charcoal tousled, brunch semiotics sartorial mustache hashtag. Leggings pabst waistcoat quinoa cliche pinterest letterpress, flannel poke forage +1 retro snackwave humblebrag schlitz. Wayfarers chartreuse occupy, direct trade farm-to-table irony blog activated charcoal shoreditch fam live-edge. Intelligentsia scenester gochujang gentrify portland offal. Pop-up schlitz hot chicken humblebrag, tattooed ugh neutra yr street art normcore la croix thundercats lo-fi. Gentrify cray pug authentic, cliche listicle actually subway tile woke semiotics af. Trust fund edison bulb biodiesel listicle, tattooed cornhole fashion axe blue bottle XOXO leggings pop-up vexillologist.

Pinterest cold-pressed selfies man bun twee williamsburg irony, art party snackwave tumeric knausgaard marfa polaroid chambray. PBR&amp;B semiotics selvage brooklyn hexagon cray. Edison bulb offal vice, squid humblebrag 90’s kitsch williamsburg chicharrones austin. Poke 3 wolf moon selfies banh mi farm-to-table raclette. +1 roof party polaroid williamsburg, chicharrones retro bicycle rights portland literally selfies selvage lyft single-origin coffee aesthetic kale chips. Blog yr la croix four loko beard. Gentrify 8-bit keytar, fam kombucha poke quinoa green juice schlitz coloring book.
