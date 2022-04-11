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

<!-- Add a single line of comment to prevent the blog post post index page from including the following text. -->

<table style="height: 224px; margin-left: auto; margin-right: auto; border-collapse: collapse; border: none;" width="100%">
<tbody>
<tr>
<td style="width: 106px; border-collapse: collapse; border: none;"><img style="display: block; margin-left: auto; margin-right: auto;" src="/assets/images/robbins.jpeg" alt="" width="200" height="300" /></td>
<td style="width: 106px; border-collapse: collapse; border: none;"><img style="display: block; margin-left: auto; margin-right: auto;" src="/assets/images/monro.jpeg" alt="https://i.picsum.photos/id/373/200/300.jpg" width="200" height="300" /></td>
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

