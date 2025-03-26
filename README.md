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

*Figure 1. 6 images detailing the stages of creating the melting klandle simulation. The first image shows the initial sculpt of the klansman. The second image shows my initial simulation using actual candle melting as a basis. The third image is the rendered version of the first simulation. The fourth image is the initial version of my second simulation that instead looks to maintain the initial structure while melting. The fifth image is my final simulation that combines the realistic simulation and the one that maintains structure. The sixth image is the final render of that simulation.*

<!-- Abstract -->
## Abstract
This project is a study looking to find the best method to simulate the effect of a melting candle in a detailed mesh object, specifically the face of a Klansman. The simulations will be done in 3 iterations. The first analyzing how a candle melts, the second, how to maintain structure in a melting simulation, and the last will combine the 2 for a combined structured, yet accurate result. The results of this study will inspire the design of the Klandle monster in my MFA Capstone Project, a video game called Haint.

[![4-comma][images-fig2]](https://example.com)

*Figure 2. Image of the reference sheet for the Klandle monster from Haint. Features images of melting flesh, candles, and klansman that are the inspiration for the sculpt and melting simulations.* 

<!-- Introduction and Related Works -->
## Introduction and Related Works

[![4-comma][images-fig3]](https://example.com)

*Figure 3. An image of simulated point-based fluid simulation in-progress in Houdini. An image of the surface maintenance graphic from the Surface Turbulance paper [3]*

The Klandle monster is a recreation of a KKK member whose flesh is made of candle wax and is melting in hellfire. In order to accurately simulate such a creature I have to study the ways in which wax melts and simulate it in an aesthetically pleasing way. 

Wax as a material initially melts, flows, and then re-solidifies [1] when heated and cooled. The shape and container of the wax can change its melting properties [2] and once a wax turns to a liquid state it can be difficult to simulate the turbulence variation in its surface to a high fidelity [3] , variation of which will be retained in its re-solidified state. 

This study uses point-based FLIP [3] simulation in Houdini and a bump map utilizing (equation) as an equation to weight the turbulence of nearby points into a smoother and higher resolution simulation [3].  The simulations are generated in 3 phases: the first testing the best parameters for generating a life-like candle simulation (density, viscosity, etc.), the second creating a simulation that visibly maintains the original geometry, and the third combining the two previous iterations to create a final simulation that maintains both form as well as accuracy. 

## Methodology


 (300)

[![4-comma][images-fig4]](https://example.com)

*Figure 4. A video capture of the first simulation focused upon accurate candle creation.*

[![4-comma][images-fig5]](https://example.com)

*Figure 5. A video Capture of the second simulation focused upon maintaining form accuracy*

[![4-comma][images-fig5]](https://example.com)

*Figure 5. A video Capture of the final simulation*

## Result and Future Work
I found that some characters were harder to recreate than others. It only took one prompt to generate the Incredible Hulk (see Figure 4.) but it took 14 prompts and re-wordings to get something poorly approximating Mickey Mouse before I gave up on the effort to generate the real deal. It seems that certain IPs are better protected than others. Whether due to repeated attempts by users to generate them or the litigiousness of the owners, one can only speculate. I would like to test the limits of this more with lesser-known properties in the future. (200)
## Conclusion
In conclusion, Generative AI has a fundamental problem with plagiarism that will continue to cause issues despite the changes being attempted to fix it. This plagiarism is disrespectful to artists and unethical and will take a change in attitude and lots of work and money to fix. (100)

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
