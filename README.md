# Docker PHAN

A utility for rapidly deploying [PHAN](https://github.com/phan/phan) for PHP apps.

Includes: 
 * PHP v7.4
 * Latest php-phan
 * ext-ast

It is based off of [**phpexperts/dockerize**](https://github.com/phpexpertsinc/dockerize-php).

# Installation

    composer require --dev phpexperts/docker-phan 

### Installation Video

https://www.youtube.com/watch?v=M32VDy5K_xU&feature=youtu.be

### Configure your PATH

Ensure that your profile PATH includes `./vendor/bin` and that it takes priority over any other directory that may include a php executable:

    PATH=./vendor/bin:$PATH

# Running

Run as normal, per the [phpan documentation](https://github.com/phan/phan).

# About PHP Experts, Inc.

[PHP Experts, Inc.](https://www.phpexperts.pro/), is my consultation company. It's a small company of a half dozen 
highly skilled Full Stack PHP devs, including myself, whom I place at 1099 positions at other corporations. We fill both 
long-term positions and, for crazy devs like me, short-term. If you ever wanted to work on a different project/company 
every few months or even weeks, anywhere in the continental U.S., Europe, or South East Asia, it's fantastic.  

Since 2015, I have set up branches in Las Vegas, Houston, the UK, Dublin, Costa Rica, Colombia, India, and the Philippines. 
If someone has a work auth in any of those places, we can place you almost anywhere you want. I travel 50% of the time 
out of choice. All over the world.

Plus, no taxes if you spend 6+ months (or a year, if you're American) out of your country. 
