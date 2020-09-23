<div align="center">

## Increase your game's FPS tips


</div>

### Description

Increase your game's FPS, coding tips, game tips, mesh tips, etc, might help you out a bit, i know they all greatly affected the way i code VB games, vote if you want, hope it helps
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[George E\.](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/george-e.md)
**Level**          |Beginner
**User Rating**    |4.9 (49 globes from 10 users)
**Compatibility**  |VB 6\.0
**Category**       |[Games](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/games__1-38.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/george-e-increase-your-game-s-fps-tips__1-57743/archive/master.zip)





### Source Code

```

<p class=MsoNormal>Version .01a - update #1</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>A few tips to speed up your games frame rate a bit, it's
amazing that some of this makes so much of a difference.<span
style='mso-spacerun:yes'>  </span>Just off the top of my head or taken from
sources, maybe you agree maybe you don’t, they all work for me, and I've run into
a lot of posts here on PSC that say &quot;my frame rate is so low&quot; etc so
here's my two cents (that’s right no spell check :) )</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Thanks <span class=SpellE>psc</span> and everyone who has
ever posted here, persistantrealities.com, vbspeed.com, tv3d, unreal <span
class=SpellE>sdk</span>, ogre <span class=SpellE>sdk</span>, and everyone else
in the world - Gandolf the Gui</p>
<p class=MsoNormal><span class=GramE>if</span> you don’t fit into this category
and I’ve forgotten to mention you than tuff luck</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span class=GramE>vote</span> or don’t it’s just here to
help people out</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span class=GramE>this</span> is not actual source code so
don’t say “it doesn’t compile”</p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal>Do Loops:</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>They are easy enough to understand and much easier and
faster than timers.</p>
<p class=MsoNormal><span class=GramE>i.e.</span></p>
<p class=MsoNormal>do while 'the escape key is not pressed' or 'the level is
still running'</p>
<p class=MsoNormal>''</p>
<p class=MsoNormal>loop</p>
<p class=MsoNormal>very simple</p>
<p class=MsoNormal>and always in your loop you need to have a do events, one
and only one do events</p>
<p class=MsoNormal>If you are making a single player game than you might want
to think about capturing the user input and only executing your loop when input
has fired, this method is death (bad thing) on multiplayer games</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>At the beginning of each loop reset your <span class=SpellE>TimeElapsed</span>
Variable, with that you have an exact count and are able to do things like
physics, motion of any kind, and many other things.<span
style='mso-spacerun:yes'>  </span>Truly much easier than a timer once you get
the hang of it.</p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal>In-line vs. modularized code</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Crazy enough, but (as per vbspeed.com, and
persistantrealities.com) inline code is faster than modularized code</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal>Variables</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span class=GramE>always</span> use option explicit and
declare all variables and never use global </p>
<p class=MsoNormal><span class=GramE>always</span> declare your constants (but
never as 16-bit <span class=SpellE>integers,varient,object</span> or anything
non-32 bit)</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Never...never...never use<span style='mso-spacerun:yes'> 
</span>'as object' or 'as variant' or 'as any', amazingly slow</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Most of us have 32-bit processors a few might have the 64's
let alone the $$$ for one</p>
<p class=MsoNormal>A longs and singles are 32 bits, integers are not, wee, use
longs and singles </p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>i.e.</p>
<p class=MsoNormal>dim i as integer</p>
<p class=MsoNormal>for i = 0 to 1000</p>
<p class=MsoNormal>next i</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>should read:</p>
<p class=MsoNormal>dim i as long</p>
<p class=MsoNormal><span class=GramE>for</span> i = 0 to 1000&amp;</p>
<p class=MsoNormal>next i</p>
<p class=MsoNormal>(no, the i after next .. &quot;next i&quot; doesn't change
the speed of anything)</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>**and**</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>VB has to treat all numbers as individual entities so
declare your numbers!!!</p>
<p class=MsoNormal>(<span class=GramE>yes</span>, you read me right, declare
your numbers!)</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span style='mso-spacerun:yes'>   </span>Type<span
style='mso-spacerun:yes'>      </span>Character</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>   </span>Integer<span
style='mso-spacerun:yes'>   </span>No character</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>   </span>Long<span
style='mso-spacerun:yes'>      </span>&amp;</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>   </span>Single<span
style='mso-spacerun:yes'>    </span>!</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>   </span>Double<span
style='mso-spacerun:yes'>    </span>#</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>   </span>String<span
style='mso-spacerun:yes'>    </span>$</p>
<p class=MsoNormal>//</p>
<p class=MsoNormal>A=5</p>
<p class=MsoNormal>B=5</p>
<p class=MsoNormal>C=(A+B) * 2</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>vs.</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>dim A as long</p>
<p class=MsoNormal>dim B as long</p>
<p class=MsoNormal>dim C as long</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>A=5&amp;</p>
<p class=MsoNormal>B=5&amp;</p>
<p class=MsoNormal>C=(A+B)*2&amp;</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span style='mso-spacerun:yes'>  </span>With Variant (no Declare)
: 3.5 secs</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>  </span>Without Variant
(declared as Long) : 1.9 secs</p>
<p class=MsoNormal>//</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><span class=GramE>dynamic</span> array fallout:</p>
<p class=MsoNormal>should you use dynamic arrays, of course you should, should
you keep appending to the <span class=SpellE>ubound</span><span
style='mso-spacerun:yes'>  </span>(<span class=SpellE>ubound</span>(<span
class=SpellE>myArray</span>)) +1 for things such as projectiles and the like,
the answer is no, iterate through your array, if an object in your array is
past the state of usefulness i.e. has hit something, reuse it, remember, the
larger an array the slower it is, if your character just spent 20 rounds and
they are all flying through the air and he/she keeps firing, than yes, append
to the <span class=SpellE>ubound</span>, iterating is slow when compared to
appending constantly, but when you finally do have to iterate the array and now
you’ve appended to it 100,000 times and poof your game just halts you’ll
understand what I’m talking about.</p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Redundant coding: the last nail in the coffin</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Private declare function iLoveSocks( HowMany as long ) as
long</p>
<p class=MsoNormal>iLoveSocks = HowMany ^ 45&amp;</p>
<p class=MsoNormal>End function</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Private sub blah()</p>
<p class=MsoNormal>Dim A as long</p>
<p class=MsoNormal>Dim B as long</p>
<p class=MsoNormal>Dim C as long</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>a = iLoveSocks(1000)</p>
<p class=MsoNormal>B = iLoveSocks(1000)</p>
<p class=MsoNormal>C = iLoveSocks(1000)</p>
<p class=MsoNormal>End sub</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>is utterly and completely wrong and will figuratively make a
60fps game run at 5</p>
<p class=MsoNormal>It should read</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Private sub blah()</p>
<p class=MsoNormal>Dim A as long</p>
<p class=MsoNormal>Dim B as long</p>
<p class=MsoNormal>Dim C as long</p>
<p class=MsoNormal>Dim TempVal as long</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>TempVal = iLoveSocks(1000&amp;)</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>A = TempVal</p>
<p class=MsoNormal>B = TempVal</p>
<p class=MsoNormal>C = TempVal</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>end sub</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span class=GramE>amazingly</span> quicker</p>
<p class=MsoNormal><span class=GramE>use</span> temporary variables everywhere
and anywhere that they can replace blocks of code</p>
<p class=MsoNormal><span class=GramE>a</span> practical example:</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span style='mso-spacerun:yes'>   </span>Dim X As Single, Y
As Single, Z As Single</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>   </span>X =
Cos(Deg2Rad(angle)) * 50</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>   </span>Y =
Tan(Deg2Rad(angle)) * 50</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>   </span>Z =
Sin(Deg2Rad(angle)) * 50</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span style='mso-spacerun:yes'>  </span>can be optimized
like this :</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span style='mso-spacerun:yes'>   </span>Dim X As Single, Y
As Single, Z As Single, RadAngle</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>   </span>RadAngle =
Deg2Rad(angle)</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>   </span>X = Cos(RadAngle) *
50!</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>   </span>Y = Tan(RadAngle) *
50!</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>   </span>Z = Sin(RadAngle) *
50!</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span style='mso-spacerun:yes'>  </span>When it's possible,
precompute values for expansive operations and organize them in tables. This is
usually used for the trigonometric operations Cos, Sin, Tan, <span
class=SpellE>Atn</span> etc...</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>   </span></p>
<p class=MsoNormal><span style='mso-spacerun:yes'>   </span>Dim Angle <span
class=GramE>As</span> Single</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>   </span>Dim <span
class=SpellE><span class=GramE>CosValue</span></span><span class=GramE>(</span>720)
As Single</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>   </span>Dim <span
class=SpellE><span class=GramE>SinValue</span></span><span class=GramE>(</span>720)
As Single</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>   </span>For Angle = 0 To
719 </p>
<p class=MsoNormal><span style='mso-spacerun:yes'>        </span><span
class=SpellE><span class=GramE>CosValue</span></span><span class=GramE>(</span>Angle)
= <span class=SpellE>Cos</span>(Deg2Rad(Angle / 2))</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>        </span><span
class=SpellE><span class=GramE>SinValue</span></span><span class=GramE>(</span>Angle)
= Sin(Deg2Rad(Angle / 2))</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>   </span>Next Angle</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span style='mso-spacerun:yes'>   </span>This table is
accurate at 0.5 degree. Then, to use it, you need to multiply the angle by 2.</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>   </span>To have the
approximation of the cosine of 45°, you need to use &quot;<span class=SpellE><span
class=GramE>CosValue</span></span><span class=GramE>(</span>45 * 2)&quot; and
voila... you get 0.707.... </p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span class=GramE>amazingly</span> enough people will
actually use 2 ^ 2 when hmm.... 2*2 and better yet, 2&amp; * 2&amp; is <span
class=SpellE>soo</span> much faster</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Strings:</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span class=GramE>hmm</span>... strings in VB are really
slow, amazingly slow when compared to longs or singles</p>
<p class=MsoNormal><span class=GramE>but</span>.. <span class=GramE>if</span>
you have to use them than just remember to use<span style='mso-spacerun:yes'> 
</span>Mid$, Right$, Left$, <span class=SpellE>Chr</span>$</p>
<p class=MsoNormal><span class=GramE>they</span> are 3 times faster with the $</p>
<p class=MsoNormal><span class=GramE>can</span> you do <span class=SpellE>realtime</span>,
every frame, string manipulation and keep 60fps.... <span class=SpellE>omg</span>,
no, no <span class=SpellE>no</span></p>
<p class=MsoNormal><span class=GramE>what</span> does that translate to.. <span
class=GramE>all</span> of you who want to do online multiplayer games...</p>
<p class=MsoNormal><span class=GramE>don't</span> use strings for anything let
alone packets, use bits for that, bit shifting and the like are amazingly
faster than strings</p>
<p class=MsoNormal>but........if you really have to use them......... use them
client side only and then use string tables in resources if you don’t know how
to use text graphics</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span class=SpellE>StrComp</span> <span class=SpellE>vs</span>
'String1=String2' .......persistantrealities.com</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Public Sub <span class=SpellE><span class=GramE>TestOne</span></span><span
class=GramE>()</span></p>
<p class=MsoNormal><span style='mso-spacerun:yes'>    </span>Dim strTest1 As
String, strTest2 As String</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>    </span></p>
<p class=MsoNormal><span style='mso-spacerun:yes'>    </span>strTest1 = <span
class=SpellE>UCase</span>$(&quot;all j00r b453 r b3l0nG 70 U5&quot;)</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>    </span>strTest2 = <span
class=SpellE>UCase</span>$(&quot;ALL J00r base R Bel0NG 70 U5&quot;)</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>    </span></p>
<p class=MsoNormal><span style='mso-spacerun:yes'>    </span>'//Compare</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>    </span>If strTest1 =
strTest2 Then</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>    </span>End If</p>
<p class=MsoNormal>End Sub</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Public Sub <span class=SpellE><span class=GramE>TestTwo</span></span><span
class=GramE>()</span></p>
<p class=MsoNormal><span style='mso-spacerun:yes'>    </span>Dim strTest1 As String,
strTest2 As String</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>    </span></p>
<p class=MsoNormal><span style='mso-spacerun:yes'>    </span>strTest1 =
&quot;all j00r b453 r b3l0nG 70 U5&quot;</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>    </span>strTest2 =
&quot;ALL J00r base R Bel0NG 70 U5&quot;</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>    </span></p>
<p class=MsoNormal><span style='mso-spacerun:yes'>    </span>'//Compare</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>    </span>If <span
class=SpellE><span class=GramE>StrComp</span></span><span class=GramE>(</span>strTest1$,
strTest2$, <span class=SpellE>vbTextCompare</span>) = 0 Then</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>    </span>End If</p>
<p class=MsoNormal>End Sub</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>100% faster compares <span class=SpellE>weee</span></p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span class=GramE>variable</span> length strings <span
class=SpellE>vs</span> fixed length strings</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Private <span class=SpellE>VariableLengthString</span> <span
class=GramE>As</span> String</p>
<p class=MsoNormal>Private <span class=SpellE>FixedLengthString</span> <span
class=GramE>As</span> String * 65526</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span style='mso-spacerun:yes'>        </span>For I = 1 <span
class=GramE>To</span> <span class=SpellE>lngIterations</span> '//Run test</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>            </span>'//Set an
element in <span class=GramE>the<span style='mso-spacerun:yes'>  </span>string</span>
to the desired value</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>            </span>Mid$(<span
class=SpellE>FixedLengthString</span>, I) = &quot;X&quot;</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>        </span>Next I</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span style='mso-spacerun:yes'>       </span>For I = 1 <span
class=GramE>To</span> <span class=SpellE>lngIterations</span> '//Run test</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>            </span>'//<span
class=GramE>Concatenate</span> a character to the variable length string</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>            </span><span
class=SpellE>VariableLengthString</span> = <span class=SpellE>VariableLengthString</span>
&amp; &quot;X&quot;</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>        </span>Next I</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>1000 times faster</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span class=GramE>Compiler options.</span></p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>The VB compiler has some optimizations that are somewhat
hidden to the user. Indeed they are given in the &quot;Compilation&quot; tab of
the Project settings, click </p>
<p class=MsoNormal><span class=GramE>then</span> on the &quot;Advanced
optimizations&quot; button.</p>
<p class=MsoNormal>There you see some unchecked boxes representing the
different optimizations that are NOT applied by default. Normally you might be
able to check them </p>
<p class=MsoNormal><span class=GramE>all</span>, without any problems in your
application. And it can really improve the speed of your application especially
for float computations.</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span style='mso-spacerun:yes'>  </span>Small <span
class=GramE>example :</span></p>
<p class=MsoNormal><span style='mso-spacerun:yes'>  </span>Dim <span
class=SpellE>i</span> <span class=GramE>As</span> Long</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>  </span>Dim A <span
class=GramE>As</span> Single</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>  </span>For <span
class=SpellE>i</span> = 1&amp; To 10000000&amp;</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>     </span>A = <span
class=SpellE><span class=GramE>Cos</span></span><span class=GramE>(</span><span
class=SpellE>i</span>)</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>  </span>Next <span
class=SpellE>i</span></p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span style='mso-spacerun:yes'>  </span>In VB <span
class=GramE>IDE :</span> 2.5 <span class=SpellE>secs</span></p>
<p class=MsoNormal><span style='mso-spacerun:yes'>  </span><span class=GramE>in</span>
a EXE form but without enabled optimization : 2.0 <span class=SpellE>secs</span></p>
<p class=MsoNormal><span style='mso-spacerun:yes'>  </span><span class=GramE>in</span>
a EXE with all enabled optimization : 0.02 <span class=SpellE>secs</span> !!!!</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>I think that this result is amazing enough to make you try
it yourself.</p>
<p class=MsoNormal><span class=SpellE><span class=GramE>ohh</span></span> and
always remove all of your &quot;<span class=SpellE>debug.print&quot;s</span>
weird but it makes a difference in the compiled version let alone the <span
class=SpellE>uncompiled</span></p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal>True or not <span class=GramE>True</span></p>
<p class=MsoNormal>According to the findings on persistantrealities.com and
other sites <span class=GramE>True</span> is faster than false, basically
instead of coding:</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Dim <span class=SpellE>isTheSkyRed</span> as Boolean</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>If <span class=SpellE>isTheSkyRed</span> = false then</p>
<p class=MsoNormal>‘ ‘ ‘ ‘ </p>
<p class=MsoNormal>End If</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>You would write</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>If <span class=SpellE>isTheSkyRed</span> = Not True then</p>
<p class=MsoNormal>‘ ‘ ‘ ‘ </p>
<p class=MsoNormal>End If</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Or</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>If Not <span class=SpellE>isTheSkyRed</span> then</p>
<p class=MsoNormal>‘ ‘ ‘ ‘ </p>
<p class=MsoNormal>End If</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Both examples are faster than saying False, I went “<span
class=SpellE><span class=GramE>hugh</span></span>?!?” the first time I saw that
one too.</p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>DirectX <span class=SpellE>vs</span> <span class=SpellE>BitBlt</span>,
<span class=SpellE>setpixel</span> etc</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span class=GramE>for</span> those of you who <span
class=SpellE>dont</span> know it as of yet, Direct X is just plainly much
quicker than <span class=SpellE>BitBlt</span> and the like, .... <span
class=GramE>if</span> used right :)</p>
<p class=MsoNormal><span class=GramE>if</span> you are going to do any kind of
picture manipulation (2D,Renders,etc) in Direct X always make sure that your
using one or more <span class=SpellE>backbuffers</span></p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Visual Culling</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span class=GramE>if</span> your going to be doing any
rendering to the screen(which is just about anyone who is reading this, by this
point) than you need to understand</p>
<p class=MsoNormal><span class=GramE>that</span> certain things need to take
precedence over others in your game</p>
<p class=MsoNormal><span class=GramE>what</span> is more important to render?:</p>
<p class=MsoNormal>1. <span class=GramE>the</span> box completely out of the
users view</p>
<p class=MsoNormal>2. <span class=GramE>the</span> front of the users 3rd
person mesh</p>
<p class=MsoNormal>3. <span class=GramE>the</span> actual visual aspect of the
users 3rd person mesh</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span class=GramE>well</span> of course the actual visual
aspect of the users 3rd person mesh</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span class=GramE>make</span> sure that your not rendering
anything that the user can not see, such an easy concept but rarely used by
beginners</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Packets (multi-player)</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span class=GramE>as</span> I’ve stated earlier use bits for
packets, that’s first of all</p>
<p class=MsoNormal><span class=GramE>secondly</span>, keep it simple:</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span class=GramE>does</span> everyone need to know that
this particular user has a axe that looks a certain way, of course not, they
just need to know that when they get</p>
<p class=MsoNormal><span class=GramE>hit</span> with it, it takes off X
damage.<span style='mso-spacerun:yes'>  </span>The same goes for two players
half a world away from each other, they absolutely don’t need to know when the
other one opens a door or jumps or almost anything for that matter, except
global game changes, what’s changing in the field of view of the users
character/camera is all that matters.</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span class=GramE>in-game-loop</span> chat</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span class=GramE>remember</span> what <span class=SpellE>i</span>
said about real-time string manipulation..... <span class=GramE>don’t</span> <span
class=SpellE>don’t</span> <span class=SpellE>don’t</span></p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>/ vs. \ weird stuff</p>
<p class=MsoNormal><span class=GramE>apparently</span> / is much <span
class=SpellE>much</span> faster than \</p>
<p class=MsoNormal>*** update ***</p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Verdana'>Also, the
&quot;\&quot; and &quot;/&quot; are completely different operations. One is
regular division, resulting in a decimal, and the other returns an integer. <span
class=GramE>for</span> example: X \ Y = <span class=SpellE>Int</span>(X / Y)<o:p></o:p></span></p>
<p class=MsoNormal><span style='font-size:10.0pt;font-family:Verdana'>***update***
-much thanks to <a
href="http://www.planet-source-code.com/vb/feedback/EmailUser.asp?lngWId=1&amp;lngToPersonId=2274451481&amp;txtReferralPage=http%3A%2F%2Fwww%2Eplanet%2Dsource%2Dcode%2Ecom%2Fvb%2Fscripts%2Fshowcode%2Easp%3FtxtCodeId%3D57743%26lngWId%3D1"><span
class=SpellE><!xmp>Gandolf_The_GUI</span></a></span></p>
<p class=MsoNormal><span class=GramE>and</span></p>
<p class=MsoNormal><span class=GramE>x</span> / 1 is much faster than <span
class=SpellE>Cint</span>(number)</p>
<p class=MsoNormal>40% faster</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Division vs. Multiplication:</p>
<p class=MsoNormal>(persistantrealities.com)</p>
<p class=MsoNormal>Public Sub <span class=SpellE><span class=GramE>TestOne</span></span><span
class=GramE>()</span></p>
<p class=MsoNormal><span style='mso-spacerun:yes'>    </span>Dim <span
class=SpellE>lngReturn</span> As Long</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>    </span>Dim Action <span
class=GramE>As</span> Long</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>    </span>Action = 0.25 </p>
<p class=MsoNormal><span style='mso-spacerun:yes'>    </span><span
class=SpellE><span class=GramE>lngReturn</span></span> = 10 * Action</p>
<p class=MsoNormal>End Sub</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Public Sub <span class=SpellE><span class=GramE>TestTwo</span></span><span
class=GramE>()</span></p>
<p class=MsoNormal><span style='mso-spacerun:yes'>    </span>Dim <span
class=SpellE>lngReturn</span> As Long</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>    </span>Dim Action <span
class=GramE>As</span> Long</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>    </span>Action = 4</p>
<p class=MsoNormal><span style='mso-spacerun:yes'>    </span><span
class=SpellE><span class=GramE>lngReturn</span></span> = 10<span
style='mso-spacerun:yes'>  </span>Action</p>
<p class=MsoNormal>End Sub</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span class=SpellE><span class=GramE>ohh</span></span> a
mere 400% faster with multiplication</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>IIF vs. If then</p>
<p class=MsoNormal>IIF is something like 70% slower</p>
<p class=MsoNormal><span class=GramE>always</span> end your if statements with
end if</p>
<p class=MsoNormal><span class=GramE>i.e</span>. none of this: if x = Z then x
= Y</p>
<p class=MsoNormal><span class=GramE>always</span> expand it</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span class=GramE>process</span> and thread priority</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span class=GramE>does</span> it really matter if your full
screen and at normal priority, crazy but true, yes</p>
<p class=MsoNormal><span class=GramE>grab</span> a little process priority code
and bump it up when your loop is running makes a difference</p>
<p class=MsoNormal><span class=GramE>does</span> process priority matter when
your in windowed mode, so much that it might boost your game 10fps or more</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>3D:</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>when making a mesh realize what part of the mesh is going to
be seen most and capitalize on that, what does low poly really mean, it means
however many <span class=SpellE>polys</span> you can use and still keep 60fps <span
class=SpellE>vsynched</span> with everything else in the scene, don’t let
anyone tell you that it means 100 poly characters or anything else for that
matter, balance it, if you really want to be cool about it either use 3
different complexity models for items shown dependant on camera distance (DOF
depth of field), but the best way is to incorporate a LOD, Level of Detail,
component to your render queue, look it up</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span class=GramE>can</span> your projectile mesh be
replaced with a fixed graphic billboard, if so, do it</p>
<p class=MsoNormal>(<span class=GramE>billboard</span> = a 1x1 plane with the
normal always facing a reference point with a graphic texture on it)</p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>1 single texture map vs. <span class=SpellE>multimaps</span>:</p>
<p class=MsoNormal>in very many 3d programs, <span class=SpellE>maya</span>,
3dsmax, <span class=SpellE>milkshape</span> you can use something called <span
class=SpellE>multimaps</span> and they end up making it much easier in the 3d
program, but when you transfer your mesh over as mdl<span class=GramE>,x,3ds</span>,
etc the materials start to pile up, basically if your program has to load 10
one MB <span class=SpellE>tex</span> files versus 1 two MB file obviously the
latter is preferable, UNWRAP all your meshes and bake them out!</p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Again, you can use strings to identify just about anything
such as the mesh title, name, texture name, file name, etc, if you’ve read
through this whole thing than you know you’ll get the shame sign from me if you
do, let alone a low frame rate.<span style='mso-spacerun:yes'>  </span>If you
need to know who “owns” this particular projectile or whatever, just use a <span
class=GramE>number(</span>long) to do so, it might make your coding a bit
harder but it will save a frame or 10 in the long run.</p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Walls, Ceiling, Floors:</p>
<p class=MsoNormal>If I could ask the god of <span class=SpellE>BSPs</span> why
you have to use boxes instead of planes for your walls, ceiling, and floors
than I would, it is for this reason only that I don’t use <span class=SpellE>bsps</span>
(there are others but I digress<span class=GramE>) .</span><span
style='mso-spacerun:yes'>  </span>Use planes whenever possible it might be a
little tricky for you to line them up correctly but in the long run, when you
take a 6 sided box versus a 1 sided plane and multiply that by an entire level
that might come out to 1000 or more <span class=SpellE>polys</span> (actually
displayed at one time (culling, <span class=SpellE>fov</span>, <span
class=SpellE>dof</span>) ) saved.</p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Foliage: a game maker and killer, everyone loves a lush
scene except when it kills frame rates.<span style='mso-spacerun:yes'> 
</span>Use multiple 1x1 planes with scripted animated textures, rotated around,
for plants, trees, etc</p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Lights:</p>
<p class=MsoNormal>Does your mesh ever really need direct dynamic illumination,
probably not, pre-compute your light maps for everything, and use a shadow plane
for your character<span class=GramE>,<span style='mso-spacerun:yes'> 
</span>for</span> we all know a 3d game is nothing without shadows, if you
really must use dynamic lighting, remember that its extremely costly and only
use it on objects visible to the user.<span style='mso-spacerun:yes'> 
</span>At one time I had the thought that I could use one dynamic light to
constantly be on the user character and to project the shadow for it as
well.<span style='mso-spacerun:yes'>  </span>It worked, but at the cost of a
base 5 frames per second, so I had to take that back from somewhere else, it
ended up being the sound, and that ended up being bad so I went to the A.I. and
lowered that, it is a perpetual balancing act, remember that.</p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Reflections:</p>
<p class=MsoNormal>If you don’t know, reflections are done with multiple scene
cameras, and multiple cameras means multiple rendering, but there is help,
rather than halving your frame rate, only have the reflection camera render
every 3<sup>rd</sup> frame or so, depending on your tastes, buffer it out and drop
the resolution on the buffer and flip it back, you lose the perfect
reflections, but you keep your player playing.</p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span class=SpellE>Ragdoll</span>:</p>
<p class=MsoNormal><span class=SpellE>Oou</span> ragdoll, soo cool, right, well
if you didn’t know, any kind of physics, solid, sliding, cloth, softbody, and
especially ragdoll, take an immense amount of processing power, the work around
to this is absolutely not to use the actual mesh, yep, use invisible extremely
basic meshes, or even better than that pure variables and math to do your
interactions.</p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span class=SpellE>Keyframe</span> vs. Predefined bone
animation:</p>
<p class=MsoNormal><span class=SpellE>Keyframe</span> animation is at this
point basically very slow to use by just about any engine let alone one
optimized for it.<span style='mso-spacerun:yes'>  </span>Use predefined bone
animation and with most 3d character editors you can even assign what
animations are blended together, easy as pie</p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Bad Fog vs. Good Fog</p>
<p class=MsoNormal>Can there be bad fog, yep, but only when it’s used wrong,
fog is basically there to either set an atmosphere for a game or to exclude
objects from the render, hint, hint, “boy <span class=GramE>its</span> foggy,
but wow I’m getting a constant 60 frames per second” is what you balance
against.<span style='mso-spacerun:yes'>  </span>And really, and I can’t express
this enough, don’t forget to exclude the completely fogged in objects from the
render.<span style='mso-spacerun:yes'>  </span>Exponential vs. Linear, like
anything, exponential is prettier but much more costly… balance.</p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Scripts:</p>
<p class=MsoNormal>Wow, I can script actions and A.I. and my game can just read
it from external files, super cool, and <span class=SpellE>uuber</span> slow,
scripts=strings=death, hardcode it unless the point of your game is to let the
user mess with it, don’t be lazy.</p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Water:</p>
<p class=MsoNormal>Dynamic water, a big fat no, non-dynamic but visually
appealing water, <span class=GramE>of<span style='mso-spacerun:yes'> 
</span>course</span>.<span style='mso-spacerun:yes'>  </span>Does your water
need to ebb and flow, if so remember that the complexity of the “land” affects
how good the water looks when it ebbs and flows, not the complexity of the <span
class=GramE>water.</span><span style='mso-spacerun:yes'>  </span>Pretty
waterfalls, yep, they’re great, but only if you use pre-rendered scripted
animated textures with alpha channels on layered low poly planes, believe me,
it looks just like you really used the crazy 3000 particles to do it, and no
you can not do 3000 particles and still well, do anything.</p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Tiles:</p>
<p class=MsoNormal>A wonderful thing if done right in 2D or pseuto-2D games, if
you don’t know what a matrix is read for a week until you dream about them,
because if your reading your tile levels from the registry let alone <span
class=SpellE>ini</span> files than I bet your scratching your head and
wondering why your level loads so slowly.</p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>3D sound:</p>
<p class=MsoNormal>No game needs CD quality sound, really, while 50 projectiles
are coming at your character they <span class=GramE>wont</span> really notice
the difference between a bit rate of 256 or 92 or 32bit audio vs. 8 or 16
bit.<span style='mso-spacerun:yes'>  </span>As a general rule, more low quality
3d sounds are always preferable to a very few very high quality 3d sounds.<span
style='mso-spacerun:yes'>  </span>Music is exactly the same, keep it low
quality unless you actually have to.<span style='mso-spacerun:yes'>  </span></p>
<p class=MsoNormal>Windows media player vs. direct sound <span class=SpellE>vs</span>
<span class=SpellE>winMCI</span></p>
<p class=MsoNormal>Windows media player = don’t use it</p>
<p class=MsoNormal>Direct sound = easiest</p>
<p class=MsoNormal><span class=SpellE><span class=GramE>winMCI</span></span> =
best but very complex to implement</p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal><span class=GramE>A.I.</span></p>
<p class=MsoNormal>One of the most costly things about games, even more than
polygon count, yep, if your going to use neural networks, genetic <span
class=GramE>algorithms ,</span> A* path finding, or any of the multitude of
A.I. out there, you just can not be liberal with it.<span
style='mso-spacerun:yes'>  </span>If a computer controlled character will only
end up dying after 10 seconds of game time does it really need to be able to
die well and do college level calc 3 hmm I don’t believe so.<span
style='mso-spacerun:yes'>  </span>Use it where it is necessary.</p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Questions that I’ve been asked:</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Q:<span style='mso-spacerun:yes'>  </span>Can I do my math /
sound / etc in a separate thread to increase my frame rate?</p>
<p class=MsoNormal>A:<span style='mso-spacerun:yes'>  </span>Can you get VB to
run stable with more than one thread, if you can go for it, if you can’t don’t,
will it make a difference, nope</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Q:<span style='mso-spacerun:yes'>  </span>What is the main way
to increase my frame rate?</p>
<p class=MsoNormal>A:<span style='mso-spacerun:yes'>  </span>If you only do one
thing from what I’ve written here, it should be to eliminate redundant coding.</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Q:<span style='mso-spacerun:yes'>  </span>Should I use
module level variables (private), sub level variables (dim), or public
variables?</p>
<p class=MsoNormal>A:<span style='mso-spacerun:yes'>  </span>From what I’ve
seen if you can put everything into one module (bas) with a sub main, and
create your form at runtime(windowed) or just do full screen it is really going
to help speed things along, it will also make your coding a headache though.<span
style='mso-spacerun:yes'>  </span>Remember, inline is faster.</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Q:<span style='mso-spacerun:yes'>  </span>Is there an easy
way to make animated X files in my favorite 3d animation program?</p>
<p class=MsoNormal>A:<span style='mso-spacerun:yes'>  </span>Not really, they
all have the X exporter, some better than others.</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Q: Should I use <span class=SpellE>vSync</span> or not?</p>
<p class=MsoNormal>A:<span style='mso-spacerun:yes'>  </span>Develop your game
without it, and if you can get your frame rate higher than the standard 60 than
go ahead and implement it, just keep in mind that some people out there use a
refresh rate of 110 or above, can your game pull that off, why even ask,
implement code to switch the users refresh rate to 60 when your game starts,
use <span class=SpellE>vsync</span>, and set it back when they exit, they’ll
never know, and your game will run super smooth on just about anyone’s decent
or better system.</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Q:<span style='mso-spacerun:yes'>  </span>Why can’t I even
use the standard teapot primitive in my BSP project, I get errors.</p>
<p class=MsoNormal>A:<span style='mso-spacerun:yes'>  </span>Do you think any
of the high-end games of today use <span class=SpellE>BSPs</span>, if you do
your wrong<span class=GramE>..</span></p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Q:<span style='mso-spacerun:yes'>  </span>Can VB really make
games as fast as C++</p>
<p class=MsoNormal>A:<span style='mso-spacerun:yes'>  </span>They both get
compiled into ASM, but VB <span class=SpellE>f’ks</span> around a bit too much
to make it tight ASM, with some of the things that I’ve previously stated you
can tighten it up a bit (declared numbers, etc).</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Q:<span style='mso-spacerun:yes'>  </span>If I use inline <span
class=SpellE>asm</span> in <span class=SpellE>vb</span> will it make a
difference?</p>
<p class=MsoNormal>A:<span style='mso-spacerun:yes'>  </span>If you can write
your own ASM than why are you writing this game in VB in the first place?</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Q:<span style='mso-spacerun:yes'>  </span>Can I apply a <span
class=SpellE>photoshop</span> like filter to my render <span class=SpellE>backbuffer</span>
each render pass to get whatever effect?</p>
<p class=MsoNormal>A:<span style='mso-spacerun:yes'>  </span>Yes and no, yes in
the fact that if your using a DX9 script to do it pre-flip than yes, if your
using just about anything else, nope, not even the super cool motion blur,
script or bust.</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Q:<span style='mso-spacerun:yes'>  </span>Witch is better,
user types or single variables</p>
<p class=MsoNormal>A:<span style='mso-spacerun:yes'>  </span>Single variables
are quicker, but unless you want your game to be 10 years in the making at the
gain of 1/100 a frame a second than just use user types, just remember to type
them as 32 bit variables.</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>_______________________________________________________________________</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Like I’ve said before, this is all just opinion and <span
class=GramE>conjecture,</span> it works for me, believe it or not.</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>If you think that you have better ideas on any of this than I
completely welcome you to write your own article on it, in fact that would be
great, let alone leave your opinions here.</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>Thanks<span class=GramE>,.</span></p>
<p class=MsoNormal>G</p>
<p class=MsoNormal><o:p>&nbsp;</o:p></p>
<p class=MsoNormal>P.S.<span style='mso-spacerun:yes'>  </span>Just about
everything I know about all of this I learned or started off on the, well one
of the feet, here on PSC, yep, I’m addicted.</p>
```

