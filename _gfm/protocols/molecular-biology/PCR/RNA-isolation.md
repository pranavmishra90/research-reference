# mRNA Isolation
Pranav Kumar Mishra
Oct 3, 2023

## Protocol

### Lyse samples and separate phases

1.  Add
    ![0.5\\mL](https://latex.codecogs.com/svg.latex?0.5%5C%20mL "0.5\ mL")
    of TRIzol into an Eppendorf tube containing each sample
2.  Transfer the contents to a mortar. Add
    ![50\\mL](https://latex.codecogs.com/svg.latex?50%5C%20mL "50\ mL")
    of liquid nitrogen
    (![LN_2](https://latex.codecogs.com/svg.latex?LN_2 "LN_2")) and
    grind the sample. Repeat with additional
    ![LN_2](https://latex.codecogs.com/svg.latex?LN_2 "LN_2"), as
    needed, grinding the sample into a fine powder.
3.  Transfer the Sample + Trizol powder into a fresh Eppendorf.
4.  Add
    ![0.3\\mL](https://latex.codecogs.com/svg.latex?0.3%5C%20mL "0.3\ mL")
    of TRIzol into each Eppendorf.
5.  Pipette mix to homogenize
6.  Incubate for *5 min* for complete dissociation of the nucleoprotein
    complex
7.  ![0.25\\mL](https://latex.codecogs.com/svg.latex?0.25%5C%20mL "0.25\ mL")
    of chloroform per
    ![1\\mL](https://latex.codecogs.com/svg.latex?1%5C%20mL "1\ mL") of
    Trizol
8.  Incubate for *2-3 min*
9.  Centrifuge the samples for *15 min* at
    ![12,000g](https://latex.codecogs.com/svg.latex?12%2C000g "12,000g")
    at
    ![4^{\circ}C](https://latex.codecogs.com/svg.latex?4%5E%7B%5Ccirc%7DC "4^{\circ}C")
10. Transfer the clear upper phase containing RNA to a fresh Eppendorf
    tube. Ensure you do not contaminate the aqueous phase by touching
    the whitish, DNA containing interphase.
11. If desired, you can store the remainder of Trizol phase containing
    DNA and Protein at
    ![-80^{\circ}C](https://latex.codecogs.com/svg.latex?-80%5E%7B%5Ccirc%7DC "-80^{\circ}C")

### RNA Isolation

1.  Add
    ![0.5\\mL](https://latex.codecogs.com/svg.latex?0.5%5C%20mL "0.5\ mL")
    of Isopropanol to the aqueous phase per 1 mL of Trizol used
2.  Incubate for *10 min*
3.  Centrifuge the samples for *15 min* at
    ![12,000g](https://latex.codecogs.com/svg.latex?12%2C000g "12,000g")
    at
    ![4^{\circ}C](https://latex.codecogs.com/svg.latex?4%5E%7B%5Ccirc%7DC "4^{\circ}C")
4.  Visualize the total RNA precipitate at the bottom of the tube
    (whitish, gel-like pellet)
5.  Discard the supernatant with a pipette
6.  Wash pellet with
    ![1\\mL](https://latex.codecogs.com/svg.latex?1%5C%20mL "1\ mL") of
    cold
    (![4^{\circ}C](https://latex.codecogs.com/svg.latex?4%5E%7B%5Ccirc%7DC "4^{\circ}C"))
    75% Ethanol per 1mL of Trizol used
7.  Vortex briefly
8.  Centrifuge the samples for *5 min* at
    ![7,500g](https://latex.codecogs.com/svg.latex?7%2C500g "7,500g") at
    ![4^{\circ}C](https://latex.codecogs.com/svg.latex?4%5E%7B%5Ccirc%7DC "4^{\circ}C")
9.  Discard the supernatant by inverting the tube in one fluid motion,
    being careful to not disturb the pellet
10. Use a vacuum centrifuge to dry the remaining amount of supernatant
    (~ *5 min*)
11. Resuspend the pellet in
    ![32\\\mu L](https://latex.codecogs.com/svg.latex?32%5C%20%5Cmu%20L "32\ \mu L")
    of RNAse-free water (molecular grade water)
12. Pipette mix to ensure complete resuspension

### Determine the RNA Yield: Nanodrop

1.  Configure the nanodrop to export to USB CSV
2.  Pipette
    ![1.5\\\mu L](https://latex.codecogs.com/svg.latex?1.5%5C%20%5Cmu%20L "1.5\ \mu L")
    of each sample into the nanodrop to measure the concentration
3.  Save the sample, giving it a name \##### RNA to USB CSV (##### is
    the 5 digit randomized study subject identification number)
4.  Paste the nanodrop readings into the corresponding CSV file / Excel
    file

<div id="tbl-nanodrop">

<table style="width:94%;">
<caption>Table 1: Select nanodrop readings</caption>
<colgroup>
<col style="width: 8%" />
<col style="width: 6%" />
<col style="width: 12%" />
<col style="width: 10%" />
<col style="width: 6%" />
<col style="width: 6%" />
<col style="width: 6%" />
<col style="width: 6%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th>Date</th>
<th>Time</th>
<th>Sample Number</th>
<th>Sample Name</th>
<th>A230</th>
<th>A260</th>
<th>A280</th>
<th>A320</th>
<th>A260/A230</th>
<th>A260/A280</th>
<th>Concentration</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>22/ 3/2023</td>
<td>4:53:26</td>
<td><pre><code>   1</code></pre></td>
<td><pre><code>2.005</code></pre></td>
<td>0.276</td>
<td>0.167</td>
<td>0.062</td>
<td>0.11</td>
<td>2.038</td>
<td><pre><code>214</code></pre></td>
<td>Demo-Sample-1</td>
</tr>
<tr class="even">
<td>22/ 3/2023</td>
<td>4:54:17</td>
<td><pre><code>   2</code></pre></td>
<td><pre><code>2.489</code></pre></td>
<td>0.363</td>
<td>0.218</td>
<td>0.067</td>
<td>0.122</td>
<td>1.96</td>
<td><pre><code>296</code></pre></td>
<td>Demo-Sample-2</td>
</tr>
<tr class="odd">
<td>22/ 3/2023</td>
<td>4:54:59</td>
<td><pre><code>   3</code></pre></td>
<td><pre><code>2.351</code></pre></td>
<td>0.351</td>
<td>0.22</td>
<td>0.06</td>
<td>0.127</td>
<td>1.819</td>
<td><pre><code>291</code></pre></td>
<td>Demo-Sample-3</td>
</tr>
</tbody>
</table>

Table 1: Select nanodrop readings

</div>

### Conversion to cDNA

Our target concentration of cDNA is 1500
![\frac{ng}{\mu L}](https://latex.codecogs.com/svg.latex?%5Cfrac%7Bng%7D%7B%5Cmu%20L%7D "\frac{ng}{\mu L}").

The least concentration of any sample is 214
![\frac{ng}{\mu L}](https://latex.codecogs.com/svg.latex?%5Cfrac%7Bng%7D%7B%5Cmu%20L%7D "\frac{ng}{\mu L}").
To obtain the target concentration, we will need to use 7.01
![\mu L](https://latex.codecogs.com/svg.latex?%5Cmu%20L "\mu L") of the
RNA previously isolated.

Our protocol will use 4
![\mu L](https://latex.codecogs.com/svg.latex?%5Cmu%20L "\mu L") of
Superscript IV VILO for each sample. The volume
(![\mu L](https://latex.codecogs.com/svg.latex?%5Cmu%20L "\mu L")) of
molecular grade water to be added is listed in the column ‘Water_uL’.

<div id="tbl-cdna-calculations">

| Sample Number |  Sample Name  | RNA (uL) | VILO (uL) | Water (uL) |
|:-------------:|:-------------:|:--------:|:---------:|:----------:|
|       1       | Demo-Sample-1 | 7.00935  |     4     |  8.99065   |
|       2       | Demo-Sample-2 | 5.06757  |     4     |  10.9324   |
|       3       | Demo-Sample-3 | 5.15464  |     4     |  10.8454   |

Table 2: Conversion to cDNA using Superscript VILO

</div>
