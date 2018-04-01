# CodePath
For CodePath course

# Project 7 - WordPress Pentesting

Time spent: **2.5** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. Title: WordPress 3.7-4.4 - Authenticated Shortcode Tags Cross-Site Scripting (XSS)
  - [x] Summary: Cross-site scripting attack. Basically, if clicked the script will launch another page which is vulnerable to attack 
    - Vulnerability types: Cross-site scripting
    - Tested in version: 4.2
    - Fixed in version: 4.2.6
  - [x] GIF Walkthrough: attack1.gif
  - [x] Steps to recreate: Go to https://wpvulndb.com/vulnerabilities/8186, copy the text in the website, and paste it on any page in wordpress. When it’s opened, it’ll pop up when you mouse over and give a notification.
  - [x] Affected source code:
TEST!!![caption width="1" caption='<a href="' ">]</a><a href="http://onMouseOver='alert(1)'">Click me</a>

    - [Link 1](https://wpvulndb.com/vulnerabilities/8186)
1. (Required) WordPress 4.1-4.2.1 - Unauthenticated Genericons Cross-Site Scripting (XSS)
  - [x] Summary: Cross-site scripting attack that when the page is loaded, the URL will show up on the page, but the cross-site scripting attack will not show. Thus, when the page loads, a message pops up and the page is vulnerable to attack. 
    - Vulnerability types: Cross-site scripting
    - Tested in version: 4.2
    - Fixed in version: 4.2.2
  - [x] GIF Walkthrough: attack2.gif
  - [x] Steps to recreate: Click the link (https://wpvulndb.com/vulnerabilities/7979) and follow the URL link embedded in the document. Copy this link and paste it into the WordPress page. When the page is loaded, the cross-site message pops up and the page will be vulnerable to attack.
  - [x] Affected source code:  http://www.example.com/wp-content/themes/twentyfifteen/genericons/example.html#1<img/ src=1 onerror= alert(1)>
    - [Link 1]( https://wpvulndb.com/vulnerabilities/7979 )
1. Title: WordPress  4.0-4.7.2 - Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [x] Summary: This attack allows someone to embed a youtube link in a page, such that when the page is launched or the link is clicked, an alert pops up. Though the youtube link looks legitimate, in reality it’s vulnerable to an attack. 
    - Vulnerability types: Cross-site scripting
    - Tested in version: 4.2
    - Fixed in version: 4.2.13
  - [x] GIF Walkthrough: attack3.gif
  - [x] Steps to recreate: Click the link (blog.securri…) and follow the URL link embedded in the document. Copy this link and paste it into the WordPress page. When the page is loaded, the cross-site message pops up and the page will be vulnerable to attack. 
  - [x] Affected source code: https://youtube[.]com/watch?v=abc<svg onload=alert(1)>
    - [Link 1]( https://blog.sucuri.net/2017/03/stored-xss-in-wordpress-core.html)


## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

