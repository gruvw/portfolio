---
layout: post
title: "Custom IoT in my house"
sub_title: "How I designed, built and programmed a full IoT system in my house from scratch."
introduction: "You can access the source code and the documentation regarding this project on the following GitHub repository:"
actions:
  - label: "Project's GitHub repository"
    icon: github
    url: "https://github.com/gruvw/maison-jung"
image: "/assets/images/posts/custom_iot_in_my_house/main.jpg"
tags:
  - Python
  - Hardware
toc: true
---

I connected regular household/garden devices in my house to control them via a smartphone.
I built the whole system from scratch without relying on any existing IoT solutions.

## 📱 Project description

<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/lamps/esp_mini.jpg" alt="Relay and ESP mini packages">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/lamps/lamp_open_mini_wemos.jpg" alt="Relay with ESP cables for lamp in box">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/lamps/mini_relay_ports.jpg" alt="Relay for ESP mini with pinout">

<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/site/site_home.jpg" alt="Mobile home screen WEB interface">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/site/site_lamps_control.jpg" alt="Lamps control WEB interface">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/site/site_schedule_control_1.jpg" alt="Scheduler day picker">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/site/site_schedule_control_2.jpg" alt="Scheduler time picker">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/site/site_schedule_invalid.jpg" alt="Scheduler invalid times validation">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/site/site_schedule_control_3.jpg" alt="Scheduler number of lamps picker">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/site/site_schedule_control_4.jpg" alt="Scheduler lamp picker">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/site/site_schedule_enable.jpg" alt="Scheduler summary of active schedules">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/site/site_stores_control.jpg" alt="Stores WEB controls for whole house">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/site/site_vanne_control.jpg" alt="Water WEB controls">

<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/stores/final_stores.jpg" alt="Three final assembled box for stores control + IR stores remote">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/stores/store_multiple_connect_green.jpg" alt="Stores inside of control box with relays connected to buttons (open remote)">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/stores/store_multiple_open.jpeg" alt="Stores remote with open box (cables inside remote)">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/stores/store_multiple_open_final.jpg" alt="Stores remote (multiple) final box open">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/stores/store_single_open.jpg" alt="Stores remote (single) final box open">

<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/telegram/telegram_feedback_1.jpg" alt="Telegram scheduler feedback messages">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/telegram/telegram_feedback_2.jpg" alt="Telegram other user feedback messages">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/telegram/telegram_lamps.jpg" alt="Telegram lamp menu">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/telegram/telegram_menu.jpg" alt="Telegram main menu">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/telegram/telegram_notification.jpg" alt="Telegram notification selection menu">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/telegram/telegram_settings.jpg" alt="Telegram settings menu">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/telegram/telegram_stores.jpg" alt="Telegram store selection menu">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/telegram/telegram_stores_action.jpg" alt="Telegram store action">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/telegram/telegram_vanne.jpg" alt="Telegram vanne selection">

<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/water/outside.jpg" alt="Outside boxes for garden control">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/water/relay_box_1.jpg" alt="Metal box inside">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/water/relay_box_2.jpg" alt="Arduino MEGA relays for vannes controls">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/water/startup_box_open_1.jpg" alt="Startup/power box insides">
<img width="20%" src="/assets/images/posts/custom_iot_in_my_house/water/startup_box_open_2.jpg" alt="Startup/power open box cables connected">
