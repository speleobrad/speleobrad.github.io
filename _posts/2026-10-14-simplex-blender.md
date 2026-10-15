---
layout: single
title:  "Simplex-blender: blending the gases you actually have"
date:   2026-10-14
categories: diving
tags:
  - gas blending
  - software
header:
  teaser: /assets/images/simplex-blender/simplex-blender-teaser.jpg
  overlay_image: /assets/images/simplex-blender/simplex-blender-teaser.jpg
  overlay_filter: 0.5
  caption: "Photo credit: [*Bilal O. / Unsplash*](https://unsplash.com/photos/red-and-white-rose-petals-UOltHXPAoyA)"
excerpt: "Simplex-blender started with two annoyances: blending the useful gas left in several cylinders, and knowing what temperature will do to the fill."
---

I have been mixing gases long enough to collect a small supply of cylinders that are not quite what I need anymore. There is some helium left in one, a bit of oxygen in another and a few cylinders of mixtures that are perfectly usable, as long as somebody figures out how to combine them.

That is where most gas blending software starts to feel a bit too optimistic. It assumes that we have pure oxygen, pure helium and a top-up gas available. It can calculate the blend from those sources, but it usually cannot take a few different scrap gases and work out how to get the mix we actually want. We either do the maths by hand or keep trying combinations in the what-if section until something looks right.

I started [Simplex-blender](https://speleobrad.github.io/simplex-blender/) to solve two problems that kept coming up.

# Scrap gas is still gas

Everybody has scrap gas somewhere. It might be a cylinder left over from the previous trip, a partial that was never quite right, or a useful mix that has been sitting in the corner because nobody wants to waste it.

A calculator that only knows about pure oxygen, pure helium and air treats those cylinders as a nuisance. In reality, each one contains oxygen, helium and nitrogen that can be useful in the next blend. The annoying part is finding the combination.

Simplex-blender lets me enter the cylinder I am starting with and several supply banks, each with its own gas composition and pressure. It then searches for a combination that can produce the requested mix, instead of making me guess one source at a time. It can use the scrap gases together, add a top-up when needed and show the pumping steps rather than only giving a final set of percentages.

That is a much better match for the way a real shelf of gas looks. The question is no longer “how much pure helium do I need?” but “what can I make from the gas I already have?”

# Temperature is not a footnote

The second problem is temperature. We all know that a cylinder gets warm while it is being filled and cools down afterwards. We also know that the pressure on the gauge is not the same thing as the amount of gas in the cylinder.

Still, most blending calculations quietly assume that the gas stays at the temperature used in the calculation. This is where the fudge factors come from: overfill the helium a little, underfill the oxygen a little, and hope that the result will be close after everything has cooled down.

Sometimes a nominal 15/55 ends up being 14/54. Sometimes it is 16/58. Sometimes we mix a cylinder to 210 bar, put it in the car, arrive at the water and discover that it is showing 190 bar. Everybody knows why this happens after the fact. The missing part is a tool that calculates it up front.

Simplex-blender includes temperature in the calculation. It can estimate what happens during the individual transfer steps, including heating while gas is moving and cooling after the fill. It can also use a real-gas model instead of assuming that oxygen, helium and nitrogen all behave perfectly at high pressure. The result is still an estimate — real equipment, flow rates, fill technique and ambient conditions matter — but it is an estimate based on the actual cylinder, equipment and temperatures rather than on a mystery correction factor.

The useful answer is not only the final blend on paper. It is also what the pressure and composition are likely to look like at the end of the transfer and after the cylinder has had time to settle.

# Try it

[Simplex-blender](https://speleobrad.github.io/simplex-blender/) is a browser-based calculator for re-blending gas from a cylinder and available supply banks. Enter the gas you have, describe the equipment and ask for the gas you want. It will find a recipe, show the transfer protocol and estimate the thermal behaviour.

It is not a replacement for analysing the finished gas or for following safe filling procedures. It is a way to stop doing the interesting parts of the calculation in your head, on paper or by repeatedly guessing in a what-if form.

Happy blending ;)
