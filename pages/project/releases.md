---
layout: default
title: Releases
permalink: project/releases
language: en
lang: en
categories: en
---
{% assign sorted_release = site.releases | sort: 'date' | reverse %}
<table>
<tr><th> Version </th><th> Date </th></tr>

{% for releases in sorted_release %}
    {% assign releasedate = releases.date | date: "%B %d, %Y" %}
    <tr>
        <td> <a href="{{site.baseurl}}/{{page.permalink}}/{{ releases.tag }}">{{ releases.tag }}</a> </td>
        <td> {{releasedate}} </td>
    </tr>
{% endfor %}

</table>
