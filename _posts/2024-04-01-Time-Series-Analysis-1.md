---
title: '[Times Series Analysis] Introduction to Time Series Analysis'
date: 2023-04-01
layout: single
categories: [Time Series Analysis]
comments: true
published: true
---

# Introduction
이번 포스팅부터는 시계열 분석(time series analysis)에 대해서 살펴본다. 사실, 시계열 분석에서 사용하는 AR(p), MA(q) 혹은 ARIMA(p, d, q)와 같은 여러 시계열 모형들은 특수한 형태의 회귀모형이라고도 볼 수 있는데 이들의 차이는 두 모형이 다루는 데이터의 특징에서 기인한다. (시계열 분석은 시계열 데이터(time series data)를, 회귀분석은 횡단면 데이터(cross-sectional data)를 다룬다.) 따라서, 회귀분석에 대한 배경지식이 있다면 이러한 시계열 모형들을 이해하는데 도움이 될 것이다.

시계열 분석 포스팅은 기본적으로 다음과 같은 참고자료를 바탕으로 작성될 예정이다.
> Forecasting: Principles and Practice 3rd Edition (2021)  
> 고려대학교 김창진 교수님의 계량경제학 II

첫번째 참고자료의 경우, online textbook의 형태로 [여기](https://otexts.com/fpp3/)에서 무료로 배포되고 있다. 두번째 참고자료의 경우, 고려대학교 정문 후문사에서 구매할 수 있다. (약 6년 전에 구매한 책이어서 현재도 판매하는 중인지는 모르겠다.)


# Stochastic Process



# Stationary


즉, 어떤 time-series에 trend나 seasonality가 있다면 이는 non-stationary time-series이다.

시계열 분석을 하기 위해서는 주어진 시계열 데이터가 정상성을 만족해야 한다. 그런데 대부분의 시계열 데이터는 정상성을 만족하지 않는다. 따라서 시계열 데이터가 정상성을 만족하도록 어떤 조치를 취해주어야 하는데 대표적으로는 차분(differencing)과 변환(transformation)으로 구분된다.

# Differencing
차분은 연속된 두 관측치의 차이를 계산하는 것이다.

$$y'_t = y_t - y_{t-1}$$

이처럼 $y'_t$는 이전 시점과 현재 시점의 관측치들의 차이로 정의되기 때문에 이전 시점의 관측치가 존재하지 않는 최초 시점($t=0$)에서는 차분이 정의되지 않는다.
