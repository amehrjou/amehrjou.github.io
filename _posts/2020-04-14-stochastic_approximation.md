---
title: 'Stochastic Approximation'
date: 2020-04-14
permalink: /posts/2020/04/stochapprox/
tags:
  - mathematics
  - optimization
  - control theory
  - machine learning
---

<!-- 
|  <img src="/images/robbins.jpeg" width="200"> |  <img src="/images/monro.jpeg" width="200" style="background-color: transparent;"> |
|---|---|
| Herbert Robbins | Sutton Monro | -->



<!-- <style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-cly1{text-align:left;vertical-align:middle}
</style> -->
<!-- <table class="tg" align="right">
  <tr>
    <th class="tg-cly1" align="center"><img src="/images/robbins.jpeg" width="200"></th>
    <th class="tg-cly1" align="center"><img src="/images/monro.jpeg" width="200" style="background-color: transparent;"></th>
  </tr>
  <tr>
    <td class="tg-cly1" align="center">Herbert Robbins</td>
    <td class="tg-cly1" align="center">Sutton Monro</td>
  </tr>
</table> -->
<!-- 
<style>
figure {
    display: inline-block;
    text-align: center;
    border: 0px dotted gray;
}
figure img {
    margin-left: auto;
    margin-right: auto;
}
figure figcaption {
    border: 1px dotted blue;
    text-align: center;
    border: 0px dotted gray;
}
</style>
<div class="container">
    <div class="center">
        <figure>
            <img src="/images/robbins.jpeg" width="10" alt='missing' />
            <figcaption>Sutton Monro</figcaption>
        </figure>
        <figure>
            <img src="/images/robbins.jpeg" width="50" alt='missing' />
            <figcaption>Herbert Robbins</figcaption>
        </figure>
    </div>
</div> -->


<table style="height: 224px; margin-left: auto; margin-right: auto; border-collapse: collapse; border: none;" width="100%">
<tbody>
<tr>
<td style="width: 106px; border-collapse: collapse; border: none;"><img style="display: block; margin-left: auto; margin-right: auto;" src="/images/robbins.jpeg" alt="" width="200" height="300" /></td>
<td style="width: 106px; border-collapse: collapse; border: none;"><img style="display: block; margin-left: auto; margin-right: auto;" src="/images/monro.jpeg" alt="https://i.picsum.photos/id/373/200/300.jpg" width="200" height="300" /></td>
</tr>
<tr>
<td style="width: 106px; text-align: center; border-collapse: collapse; border: none;">
<div>
<div>Herbert Robbins</div>
</div>
</td>
<td style="width: 106px; text-align: center; border-collapse: collapse; border: none;">&nbsp;Sutton Monro</td>
</tr>
</tbody>
</table>



Stochastic approximation is at the heart of many contmporary methods in science and engineering. The reason is simply due to the stochasticity of nature which is caused by our partial observation per se. In almost every occasion, our best bet is to obtain a noisy corrupted observation of some natural process while we are interested to estimate a target value as accurately as possible. A rigirous study of stochastic approximation stemmed from Robbins and Monro's seminal work in 50s on analysing the recursive procesure to find the root of an unknown real-valued function from its noisy corrupted evaluations. Since then, stochastic approximations have been extensively studied and used in countless areas such as images and signal processing, adaptive control, convex optimization, machine learning, reinforcement learning, and etc. In this writing, we review the theory behind stochastic approximation and point out to a few algorithm derived from it in other areas to see why they work!

