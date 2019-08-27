# SEEING THE INVISIBLE: A CROSSOVER BETWEEN ASTROPHYSICS AND COMPUTER VISION
### *For  long,  Computer  Sciences  and  related  fields  were  imagined  to  be  mutually  exclusive with the more natural sciences, such as Astrophysics. The discovery of the supermassive black hole at the centre of M87 blurs this line for good.*
Earlier  this  year,  on  the  10th  of  April,  2019,  a  team of over 200 researchers, along with the EHT (Event  Horizon  Telescope)  revealed  the  first  ever  image of a black hole for the public to see, at a press conference  in  Brussels.  Messier  87,  better  known  now as M87, one of the most massive galaxies in the observable universe, hosts this supermassive black hole  at  its  centre.  The  statistics  are  baffling:  the  black hole is at a staggering distance of 53 million light-years  from  the  earth,  and  the  supermassive  black hole at its centre is estimated to be about 2.4 billion  times  heavier  than  our  Sun.  Even  at  these  distances, the black hole image proved to be similar to  what  Einstein’s  Theory  of  General  Relativity  predicted,  thus  proving  to  be  a  major  success  for  the physics community all across the globe.
<br>But  what  truly  stands  out  in  this  major  scientific  experiment,  is  the  technological  might  that  went  behind  it.  As  Katie  Bouman,  a  computer  scientist  in  California  Institute  of  Technology,  explained,  the  feat  is  comparable  to  observing  an  orange  on  the  Moon’s  surface  from  here  on  Earth,  with  a  naked eye. To attain this extraordinary resolution, computations reveal that a telescope with a diameter around  that  of  the  earth  would  be  required.  To  overcome such a complication, a technique known as VLBI, or Very Long Baseline Interferometry was used.  An  interferometer  is  a  device  that  uses  the  interference  of  EM  waves  to  extract  information  about  them.  Interferometry  is  an  umbrella  term  that covers all such techniques.
## *Very Long Baseline Interferometry:*
VLBI  is  a  type  of  astronomical  interferometry  used  in  radio  astronomy.  In  VLBI  a  signal  from  an astronomical radio source, such as a quasar, is collected  at  multiple  radio  telescopes  on  Earth.  The distance between the radio telescopes is then calculated  using  the  time  difference  between  the  arrivals  of  the  radio  signal  at  different  telescopes.  This allows observations of an object that are made simultaneously  by  many  radio  telescopes  to  be  combined, emulating a telescope with a size equal to the maximum separation between the telescopes. The EHT implemented this by using eight ground-based  radio  telescopes  at  different  places  on  the  globe. Once the different telescopes have collected data from the black hole, the scientists would have to  combine  and  compile  the  data  using  the  VLBI  technique.
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;One  might  be  tempted  to  ask,  as  to  how  the  superposition  of  these  datasets  from  different  telescopes  occurs.  It  is  instructive  to  start  by  considering   a   simple   radio   interferometer   that   consists of two dishes pointed at the same position on  the  sky  as  shown  below.  Radio  waves  from  a  distant  cosmic  source  (e.g.,  a  star,  black  hole,  galaxy)  reach  antenna  2  (on  the  right)  a  time  τg before the other. When combined in a ‘correlator’ that  multiplies  and  averages  the  signals  together,  the output is a complex number whose magnitude is the intensity of the cosmic source and whose phase is given by (2πτgc/τ), where τ is the wavelength of  the  received  radio  waves  and  c  is  the  speed  of  light.  This  phase  is  simply  a  full  rotation  for  each  wavelength  of  extra  path  length  the  radio  waves  have  to  travel  to  reach  the  second  (more  distant)  antenna. Now we can see the relationship between interferometer phase and position on the sky: if the source changes in position on the sky by an angle of τ/dp,  (where  dp  is  the  distance  between  the  antennas projected in the direction of the source) the phase changes by a full rotation. In this sense, the  interferometer  has  an  angular  resolution,  or  magnifying power, of τ/dp, equivalent to a regular telescope  whose  diameter  is  dp.  By  adding  a  compensating delay ( τg) to the electronic system at antenna  2,  we  can  zero  the  phase  for  a  particular  direction on the sky.
<br>Except,  there  is  one  issue.  Had  the  earth  been  covered    with    radio    telescopes    all    over    its    surface,  except  only  at  8  points,  we  would  have  a   complete,   continuous   dataset   describing   the   black hole. Instead, we have separate images from 8  distinct,  faraway  points  on  the  globe,  with  a  lot  of  discontinuities  in  between  because  of  absent  telescopes.   Filling   these   gaps   was   the   biggest   obstacle in imaging the black hole.
## *The CHIRP Algorithm for Image Reconstruction*
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;To    solve    this    problem,    an    algorithm    called     “Continuous     High-resolution     Image     Reconstruction  using  Patch  priors”  or,  simply,  CHIRP  was  used.  The  development  of  CHIRP  involved  a  large  team  of  researchers  from  MIT’s  Computer   Science   and   Artificial   Intelligence   Laboratory,  the  Harvard-Smithsonian  Center  for  Astrophysics   and   MIT   Haystack   Observatory.   Due to a limited number of telescopes used on the earth, we get a dataset that is not continuous, and we can fill the missing gaps in an infinite number of ways,  but  some  images  formed  by  filling  the  gaps  are more likely to be natural renditions of a black hole, while others won’t be as likely to be so. (Fill in an example/ image) This algorithm does exactlythat- fill in the missing pieces of this puzzle to obtain the most ‘natural’ looking image. CHIRP achieves this by first combining the datasets obtained from different radio telescopes across the planet using the VLBI technique. At the output level, after filling up the images, the algorithm ranks the images in order of “likelihood” of being images of a black hole. The most likely image is then displayed. The process of filling  up  the  missing  puzzle  pieces  is  similar  to  a  forensic  sketch  artist  drawing  portraits  of  people  using limited data about the person’s face.
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The problem can also be likened to that of distinguishing three day-to-day images and asking which  one  of  them  is  more  likely  to  appear  on  a  social  media  platform,  say  Facebook.  (Provide  image) Given below are three images, a noisy one, a blurry image of a city skyline and a regular image of one. If one had to rank the three images, the most likely image to be on Facebook would be the non-blurry, non-noisy image, and the least likely image would  be  the  noisy  one,  with  the  blurry  image  in  between. We use our experience of what an image is supposed to look like in order to rank the images based on this priority.
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;But  the  issue  with  ranking  images  which  are possible candidates for a true, complete black hole image is that we have no idea of what a black hole  looks  like!  -  Hence  rendering  the  idea  of  ‘experience’ useless in this scenario. If we consider Einstein’s equations as the determining factor, then however  different  the  actual  black  hole  structure  might be, we would end up getting what we expect to see because we incorporated Einstein’s equations into  the  algorithm  too  much.  The  same  problem  would occur with using simulations of black holes to  fill  the  missing  parts  of  the  image  because  the  simulations themselves are created using Einstein’s equations.
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;To  bypass  this  issue,  computer  scientists  thought of treating the dataset from the observatory as a giant puzzle, with certain missing pieces. Then, the algorithm will fill up the missing pieces first by using  pieces  from  sample  black  hole  simulations,  then  from  other  astronomical  objects,  and  then  using  sample  image  pieces  of  everyday  lives.  In  this  way,  even  if  we  get  the  expected  image  of  a  black hole by filling in pieces of the simulation, if we were to get a similar looking picture by filling in any other piece from any non-celestial object, we could  be  more  “confident”  that  the  image  we  are  getting is close to the actual celestial object under consideration. This is similar to giving the task of drawing  a  person’s  face  to  three  different  sketch  artists  each  with  the  same  amount  of  information  the  other  is  provided  with.  If  the  three  sketches  come out to be similar enough, we could say that the ‘cultural bias’ of the different artists didn’t play a major role in the construction of the image, and hence,  the  similar  images  we  have  gotten  from  the three sketch artists is the closest to the actual picture desired from them.
<br>Before   using   the   CHIRP   algorithm   on   the   supermassive  black  hole  at  the  centre  of  M87,  they  tested  the  algorithm  on  a  simulation  of  the  black hole at the centre of our Milky Way Galaxy. The  results  they  obtained  were  affirmative  of  the  correctness  of  their  method.  The  results  of  the  reconstruction of the simulation are given below.
## *Conclusion*
The  success  of  the  Event  Horizon  Telescope  in  successfully recording the data, compiling it using the  VLBI  technique  and  then  using  the  CHIRP  algorithm  to  fill  the  missing  gaps,  is  a  telltale  sign  of  the  great  strides  humanity  is  going  to  see  in   interdisciplinary   areas   involving   Computer   Science  and  Technology  (in  this  case,  Computer  Vision)  and  the  Natural  Sciences  (Astrophysics).  The   elation   of   the   general   populace   and   the   scientific  community  at  being  finally  able  to  see  a  real  black  hole  image,  and  to  be  able  to  prove  the General Theory of Relativity is quite expected, but  an  equally  important  development  is  that  of  the increasing sophistication of the tools mankind now   possesses,   especially   in   relation   to   both   computer vision and astrophysics. All of this can be perfectly  encapsulated  in  the  words  of  Shepherd  S.  Doeleman,  the  EHT  Project  Director,  who  said,”We have achieved something presumed to be impossible just a generation ago. Breakthroughs in technology, connections between the world’s best radio  observatories,  and  innovative  algorithms  all  came together to open an entirely new window on black holes and the event horizon.”