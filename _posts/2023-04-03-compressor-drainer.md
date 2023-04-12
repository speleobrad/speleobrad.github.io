---
layout: single
title:  "Vortex drainer"
date:   2023-04-04 16:48:00 +0100
categories:
    - compressor
    - tinkering
tags: 
    - compressor
    - openscad
gallery_model:
    - url: /assets/images/drainer/model-01.png
      image_path: /assets/images/drainer/model-01.png
      title: Vortex drainer model
    - url: /assets/images/drainer/model-02.png
      image_path: /assets/images/drainer/model-02.png
      title: Modled with PET bottle thread. Note the air divertion holes inside the lid. 
    - url: /assets/images/drainer/model-03.png
      image_path: /assets/images/drainer/model-03.png
      title: Vortex drainer - detail of the lid with highligted air flow channels
    - url: /assets/images/drainer/model-04.png
      image_path: /assets/images/drainer/model-04.png
      title: Lid for 3 hoses. 
    - url: /assets/images/drainer/model-05.png
      image_path: /assets/images/drainer/model-05.png
      title: Being parametric, it can also be configured for 1 hose... 
    - url: /assets/images/drainer/model-06.png
      image_path: /assets/images/drainer/model-06.png
      title: ... or 4, if that's how much you have... 
    - url: /assets/images/drainer/model-07.png  
      image_path: /assets/images/drainer/model-07.png
      title: ... or 4, if that's how much you have... 
    - url: /assets/images/drainer/model-08.png  
      image_path: /assets/images/drainer/model-08.png
      title: ... or 4, if that's how much you have... 
gallery_printed:
    - url: /assets/images/drainer/vortex-drainer-assembled.jpg
      image_path: /assets/images/drainer/vortex-drainer-assembled.jpg
      title: Assembled Vortex drainer. Transparent PETG, Variable layer height.
    - url: /assets/images/drainer/vortex-drainer-assembly-view.jpg
      image_path: /assets/images/drainer/vortex-drainer-assembly-view.jpg
      title: Vortex drainer parts. Transparent PETG, Variable layer height.  
    - url: /assets/images/drainer/vortex-drainer-parts.jpg
      image_path: /assets/images/drainer/vortex-drainer-parts.jpg
      title: Vortex drainer parts. Transparent PETG, Variable layer height.
    - url: /assets/images/drainer/vortex-drainer-lid.jpg
      image_path: /assets/images/drainer/vortex-drainer-lid.jpg
      title: Vortex drainer lid with holes for accepting hoses from compressor condensate drain. Transparent PETG, Variable layer height.
    - url: /assets/images/drainer/vortex-drainer-parts-side-by-side.jpg
      image_path: /assets/images/drainer/vortex-drainer-parts-side-by-side.jpg
      title: Vortex drainer parts. Transparent PETG, Variable layer height.  
    - url: /assets/images/drainer/vortex-drainer-lid-inside.jpg
      image_path: /assets/images/drainer/vortex-drainer-lid-inside.jpg
      title: Air flow holes inside vortex drainer that divert the air towards ouside walls. Transparent PETG, Variable layer height.
    - url: /assets/images/drainer/vortex-drainer-in-printing.jpg
      image_path: /assets/images/drainer/vortex-drainer-in-printing.jpg
      title: Vortex drainer during printing.
    - url: /assets/images/drainer/vortex-drainer-inlet-prototype.jpg
      image_path: /assets/images/drainer/vortex-drainer-inlet-prototype.jpg
      title: Early prototype of an inlet block with air diverters. Looks cool but took ages to print. White PETG, 0.20mm.
    - url: /assets/images/drainer/vortex-drainer-with-hose.jpg
      image_path: /assets/images/drainer/vortex-drainer-with-hose.jpg
      title: Vortex drainer with fitted hose. Transparent PETG, Variable layer height.

excerpt: "After getting splashed few times by compressor condensate, I decided to build an overengineered vortex drainer."
header: 
  teaser: /assets/images/drainer/vortex-teaser.jpg
  overlay_image: /assets/images/drainer/vortex-teaser.jpg
  overlay_filter: 0.5
  caption: "Photo credit: [*Andrew Teoh / Unsplash*](https://unsplash.com/photos/8I_URI_FGu0?utm_source=unsplash&utm_medium=referral&utm_content=creditShareLink)"

---
After getting splashed few times by compressor condensate, I decided to build an overengineered vortex drainer.

# Intro 

I saw various solutions for draining the condensate from the compressor stages - from "factory" drainage buckets (regular bucket with inlet hose opening and vent holes placed in such a way that you mostly don't get splashed) to DIY solutions involving PET bottles and pocket knifes that result in flying bottles and some cursing and swearing. Some of my friends drain compressors "on the spot" resulting in wet and sligtly greasy floors, while one (dear) friend uses old T-shirt to "muffle the sound and collect water". You can imagine the color and smell of that cloth.

I wanted to use this as oportunity to learn OpenSCAD and I designed parametric vortex separator (overengineering at its best) to trap water and oil while allowing air to escape. 

# OpenSCAD model

I played with [BOSL2 library](https://github.com/revarbat/BOSL2) and, after banging my head against few concepts, managed to build a two-piece drainer with some configurable parameters: 
 - Size of drainer (height and diameter)
 - Number of inlet hoses and their diameter 

For extra points, I configured slopes on the the critical parts so they print easier and have added slightly expanding holes for hoses, so they self-lock as they are pushed in.

{% include gallery id="gallery_model" class="full" layout="half" caption="Looks of Vortex drainer" %}

# Printing 

Printing it turned to be a bit of a challenge as some threads look like overhangs and I really don't like supports on PETG. I tried variable layer height and ended up with few spaghetti prints, but fixed layer height seem to be working just fine. 

{% include gallery id="gallery_printed" class="full" layout="half" caption="Looks of Vortex drainer" %}

# Files and stuff

Rendered SLTs and OpenSCAD source are available on [Printables.com](https://www.printables.com/model/443598-vortex-condensate-drainer). 

Happy printing and happy draining ;) 