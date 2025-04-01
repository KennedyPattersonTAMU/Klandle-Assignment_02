# Klandle-Assignment_02
Second Assignment for Generative Art and Design at Texas A&amp;M University

<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a id="readme-top"></a>

<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->




<!-- PROJECT LOGO -->
<br />
<div align="center">
  </a>

  <h3 align="center">Simulation Study: Melting Klandle</h3>

  <p align="center">
    This project is a process study in melting simulations using Houdini in order to try to recreate the look of a candle melting while retaining the shape of the initial object throughout this process. The study is a part of the development of my MFA Capstone Project and video game Haint.
    <br />
    <a href="https://github.com/KennedyPattersonTAMU/4-Comma-Assignment_01/blob/main/PDF/Artists_Squeezed_Yonkoma.pdf"><strong>Link to PDF Report »</strong></a>
    <br />
    <br />
    <a href="https://website.com">Kennedy Patterson</a>
    &middot;
    <a href="https://sites.google.com/view/viza626/home">VIZA 626</a>
  </p>
</div>

[![4-comma][images-fig1]](https://example.com)
[![4-comma][images-fig2]](https://example.com)
[![4-comma][images-fig3]](https://example.com)
[![4-comma][images-fig4]](https://example.com)
[![4-comma][images-fig5]](https://example.com)
[![4-comma][images-fig6]](https://example.com)

*Figure 1. 6 images detailing the stages of creating the melting klandle simulation. The first image shows the initial sculpt of the klansman. The second image shows my initial simulation using actual candle melting as a basis. The third image is the mesh version of the first simulation. The fourth image is the initial version of my second simulation that instead looks to maintain the initial structure while melting.The fifth image is the mesh version of my second iteration. The sixth image is my final simulation that combines the realistic simulation and the one that maintains structure.*

<!-- Abstract -->
## Abstract
This project is a study looking to find the best method to simulate the effect of a melting candle in a detailed mesh object, specifically the face of a Klansman. The simulations will be done in 3 iterations. The first analyzing how a candle melts, the second, how to maintain structure in a melting simulation, and the last will combine the 2 for a combined structured, yet accurate result. The results of this study will inspire the design of the Klandle monster in my MFA Capstone Project, a video game called Haint.

[![4-comma][images-fig7]](https://example.com)

*Figure 2. Image of the reference sheet for the Klandle monster from Haint. Features images of melting flesh, candles, and klansman that are the inspiration for the sculpt and melting simulations.* 

<!-- Introduction and Related Works -->
## Introduction and Related Works

[![4-comma][images-fig8]](https://example.com)

*Figure 3.  An image of the surface maintenance graphic from the Surface Turbulance paper [3]*

The Klandle monster is a recreation of a KKK member whose flesh is made of candle wax and is melting in hellfire. In order to accurately simulate such a creature I have to study the ways in which wax melts and simulate it in an aesthetically pleasing way. 

Wax as a material initially melts, flows, and then re-solidifies [1] when heated and cooled. The shape and container of the wax can change its melting properties [2] and once a wax turns to a liquid state it can be difficult to simulate the turbulence variation in its surface to a high fidelity [3] , variation of which will be retained in its re-solidified state. 

This study uses point-based FLIP [3] simulation in Houdini and a bump map utilizing 

[![4-comma][images-equation]](https://example.com) 

as an equation to weight the turbulence of nearby points into a smoother and higher resolution simulation [3].  The simulations are generated in 3 phases: the first testing the best parameters for generating a life-like candle simulation (density, viscosity, etc.), the second creating a simulation that visibly maintains the original geometry, and the third combining the two previous iterations to create a final simulation that maintains both form as well as accuracy. 

## Methodology

[![4-comma][images-fig9]](https://youtu.be/X0WJpJaHfVo)

[![Video capture on Youtube](https://img.youtu.be/X0WJpJaHfVo.jpg)](https://youtu.be/X0WJpJaHfVo)

*Figure 4. A video capture of the first simulation points melting. This simulation is focused on accurately recreating the melting pattern of a candle.*

I started my project using a FLIP melting simulation in Houdini and changed the density of the fluid object to match that of a solid except for in the presence of high temperatures. I then created an heat-source with a randomly patterned surface and a high temperature so that the candle would melt only on where the source touched. I then animated the surface and position of the heat source to melt the candle in random sections from top to bottom. This method of simulation was very accurate in simulating candle melting as well as being variable in the future.

The primary issue is that the simulation completely destroys all details in the mesh so that it is impossible to tell what the original model was. My next pass would need to simulate melting while maintaining detail.

[![4-comma][images-fig10]](https://youtu.be/i8UyYToHp5Q)

[![Video capture on Youtube](https://img.https://youtu.be/i8UyYToHp5Q)](https://youtu.be/i8UyYToHp5Q)

*Figure 5. A video capture of the second simulation points melting. This simulation is focused on maintaing the details of the mesh*

I found a tutorial online that creates a mask from the temperature of the object. In places where the temperature is high the mask is active. Once a part of the model has an active mask the melting animation proceeds in a low detail version of the model and the mesh disappears in a high detail version of the model. This allows for gradients of detail in the mesh as the heat changes which adds verisimilitude to the simulation. The major issue with this second pass is that it does not  accurately melt the candle. While it is a very good overall melting simulation, it is not a very good *candle* melting simulation.

In my final iteration I attempted to combine the strengths of the previous two passes. I wanted to preserve the accuracy of the candle simulation of the first while maintaining the detail of the second. This last iteration largely ended in failure as I could not get the mask to work with the first iterations fluid simulation. As such, the two iterations of the melting simulation did not merge correctly and instead left a very fake looking end result. 

[![4-comma][images-fig11]](https://img.https://youtu.be/SFG0N-d0FFg)]

[![Video capture on Youtube](https://img.https://youtu.be/SFG0N-d0FFg)](https://youtu.be/SFG0N-d0FFg)


*Figure 6. A video capture of the shaded initial simulation*

[![4-comma][images-fig12]](https://example.com)

*Figure 7. An image sequence of frames from the shaded final simulation*

## Result and Future Work

I would like to iterate on the final pass of the combined simulations and use that final pass to create a higher poly sculpted mesh of the Klandle character. I feel as if more time and research is needed in order to achieve a truly perfect simulation. I would also like to test a way to simulate dripping down the sides of the model as I see that is a prominent part of reference that I've used throughout this project that is not replicated well in either simulation. 

I found the end result of this study to be lackluster but the process highly informative and would like to use node-based simulation as a prototyping tool in the future. I think the ability to itterate is a lot more forgiving than with physical media and saves more time than attempting to sculpt the object did. I simply need more experience with the software.

## Conclusion
In conclusion, Houdini is an excellent way of prototyping physics simulations for artistic reference and is a good way of learning how to work with diverse materials to create a better overall product. I will continue to use it in my workflow and hopefully be better equipped to tackle this challenge in the future. 

<!-- Bibliography -->
## Bibliography 
[1] Carlson, Mark, et al. “Melting and Flowing.” Association of Computing Machinery, 21 July 2002, dl.acm.org/doi/abs/10.1145/545261.545289, https://doi.org/10.1145/545261.545289. Accessed 25 Mar. 2025.

[2] Ghosh, Debasree, and Chandan Guha. “Numerical and Experimental Investigation of Paraffin Wax Melting in Spherical Cavity.” Heat and Mass Transfer, vol. 55, no. 5, 23 Nov. 2018, pp. 1427–1437, link.springer.com/article/10.1007/s00231-018-2522-0, https://doi.org/10.1007/s00231-018-2522-0. Accessed 25 Mar. 2025.

[3] Mercier, Olivier, et al. “Surface Turbulence for Particle-Based Liquid Simulations.” ACM Transactions on Graphics, vol. 34, no. 6, 2 Nov. 2015, pp. 1–10, www-labs.iro.umontreal.ca/~derek/files/surfaceWaves.pdf, https://doi.org/10.1145/2816795.2818115. Accessed 9 Feb. 2024.

[4] Teng, Yun, et al. “Eulerian Solid-Fluid Coupling.” ACM Transactions on Graphics, vol. 35, no. 6, 11 Nov. 2016, pp. 1–8, www.tkim.graphics/EULERSF/TengLevinKim2016.pdf, https://doi.org/10.1145/2980179.2980229. Accessed 26 Mar. 2025.


<!-- CONTACT -->
## Contact

Kennedy Patterson - kennedyp@tamu.edu

Personal Website: [https://kennedpatterson.artstation.com/](https://kennedpatterson.artstation.com/)




<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

This work is submitted as part of Assignment 2 for the VIZA 626 course at Texas A&M University, under the instruction of Professor You-Jin Kim, during the Spring 2025 semester.

VIZA 626 Class Website: [https://sites.google.com/view/viza626/](https://sites.google.com/view/viza626/home)

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge
[contributors-url]: https://github.com/othneildrew/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=for-the-badge
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=for-the-badge
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=for-the-badge
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/othneildrew
[product-screenshot]: images/screenshot.png
[images-fig1]: images/fig1.png
[images-fig2]: images/fig2.png
[images-fig3]: images/fig3.png
[images-fig4]: images/fig4.png
[images-fig5]: images/fig5.png
[images-fig6]: images/fig6.png
[images-fig7]: images/fig7.png
[images-fig8]: images/fig8.png
[images-fig9]: images/fig9.png
[images-fig10]: images/fig10.png
[images-fig11]: images/fig11.png
[images-fig12]: images/fig12.png
[images-equation]: images/equation.png
<video src="images/fig11.mp4" width="320" height="240" controls></video>

[Next.js]: https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white
[Next-url]: https://nextjs.org/
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-url]: https://reactjs.org/
[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[Angular-url]: https://angular.io/
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com 
