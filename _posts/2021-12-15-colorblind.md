---
title: "Exploring Color Blindness: A Shiny App Based Color Blindness Test & Filter"
tags:
  - Data Visualization
  - Data Wrangling
  - Statistical Computing
---

This project was created by Holly Cui, Parker Dingman, Sophie Dalldorf, and Kate Neal under the instruction of Professor Mine Cetinkaya-Rundel for the Fall 2021 section of [STA 313: Advanced Data Visualization](https://vizdata.org/) at Duke University.

## Introduction

Our project embarked on the goal of increasing awareness and understanding of colorblindness through a creatively designed **R-Shiny** based web application. This initiative is not just a technological endeavor but also a bridge to greater empathy and insight into the world as seen by individuals with color vision deficiencies.

Color blindness affects approximately 1 in 12 men and 1 in 200 women globally, summing up to around 300 million people. While often genetic, conditions such as diabetes, multiple sclerosis, or aging can also contribute to its occurrence. Our project zeroes in on the four most prevalent types of colorblindness: *Protanopia* (red-green), *Deuteranopia* (green deficiency), *Tritanopia* (blue-yellow), and *Monochromatism* (absence of color perception). It's important to acknowledge that our understanding of colorblindness is largely based on research conducted in Western populations, and variations may exist globally.

<p align="center" width="100%">
  <img src="/images/intro.gif" alt="Intro" width="120%"/>
</p>
<div style="text-align: right"> <i>© Rob Woods by www.allaboutvision.com.</i> </div>

Our experience in the data visualization course has underscored the critical role of color in various domains, ranging from art and aesthetics to education and scientific research. This insight inspired our project's theme and three primary objectives:

1. Educate users about the different types of color blindness.
2. Provide an immersive experience allowing users to view the world through the lens of someone with color blindness.
3. Offer a test feature to help users identify if they might be affected by one of the four main types of color blindness.

Therefore, blending educational elements with interactive features, we aims to foster greater empathy and understanding while providing valuable insights into the challenges faced by those with color blindness.

## The Math: Explained

**Mathematical Foundation of the App**: Although not the first feature encountered in our app, the math section forms the core of all the filters used throughout. Our aim was to demystify the complex linear algebra behind the color blindness filters, breaking it down into three straightforward steps: transforming RGB to LMS (long, medium, and short wave light), applying the LMS filter, and then converting back from LMS to RGB. To enhance user comprehension, we juxtaposed a clear written explanation of these steps on the left with the corresponding matrix mathematics displayed on the right. Maintaining a clean and simple layout was a crucial aspect of our design philosophy.

<p align="center" width="100%">
  <img src="/images/math.png" alt="Math" width="60%"/>
</p>

**Understanding Colorblind Physiology Through Math**: While the mathematics provides the technical foundation, we also wanted to ensure that users gain an insightful understanding of the physiology underlying color blindness. This aspect was seamlessly integrated, as comprehending the differences between long, medium, and short cones in relation to RGB space is essential to grasping the mathematical framework. Additionally, the physiology of color blindness is further explored in relation to how different cones perceive light, offering users a more profound appreciation of the causes behind various types of color blindness.

**Quantifying Colorblindness Severity**: A unique feature of our app is the ability to define and visualize varying degrees of color blindness. This concept, while not conventionally used in medical diagnostics, was essential for the functionality of our app, particularly for the sliding scale feature in the colorblind filter section. By creating a continuous variable to represent the severity of color blindness, we enabled users to adjust the filter and experience different levels of color perception challenges. This innovative approach provides a practical tool for understanding the spectrum of color vision deficiencies.










<embed src="https://tinyurl.com/colorblindapp" style="width:800px; height: 500px;">






