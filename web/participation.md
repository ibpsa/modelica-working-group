---
layout: page
title: Participation
permalink: /participation
---

<h1>Participation</h1>

There are two types of participation,
<em>individual participants</em> and
<em>sponsoring participants</em>.
There are currently
{{ site.data.individual_participants | size }} individual participants and
{{ site.data.sponsoring_participants | size }} sponsoring participants.


To receive announcements you need join this email announcement list:

<table>
<tr><td>
General Project Announcements,<br/>also used to announce meetings in the work groups.
</td><td>
<a class="btn btn-primary btn"
                style="color:white;text-decoration:none"
                href="https://github.com/ibpsa/modelica-working-group/wiki">
                Archive</a>
</td><td>
<a class="btn btn-primary btn"
                style="color:white;text-decoration:none"
                href="https://groups.google.com/g/ibpsa_modelica_working_group">
                Register</a>
</td></tr>
</table>

You don't need to be an
organizational, individual or sponsoring participant
to join this email list.
Please click the link to register.
Note that the default setting from google groups is to not receive messages; you need to change this setting
during the registration in order to received messages.

<h2>Individual Participants</h2>
<p>
Individual participants are contributors that participate in the project as is custom in other open-source projects without a pre-determined level of commitment.
</p>
<p>
The operating agents can reassess the individual participant membership annually and terminate membership if no substantial contributions are made.
</p>

<table class="table_with_header">
<thead valign="bottom">
<tr>
<th>Name</th>
<th>Affiliation</th>
<th>Country</th>
</tr>
</thead>
<tbody valign="top">
{% for participant in site.data.individual_participants %}
<tr>
  <td>
    <a href="mailto:{{ participant.contact_email }}">{{ participant.contact_name }}</a>
  {% if participant.role == "Co-operating agent" %}
  <br/>
  {{ participant.role }}
  {% endif %}
  </td>
  <td>
  {{ participant.affiliation }}
  </td>
  <td>
  {{ participant.country }}
  </td>
</tr>
{% endfor %}
</tbody>
</table>

<h2>Sponsoring Participant</h2>

Sponsoring participants are individuals or organizations that fund the project.

<table class="table_with_header">
<colgroup>
<col width="70%" />
<col width="15%" />
<col width="15%" />
</colgroup>
<thead valign="bottom">
<tr>
<th>Company</th>
<th>Country</th>
<th>Contact</th>
</tr>
</thead>
<tbody valign="top">
{% for participant in site.data.sponsoring_participants %}
<tr>
  <td>
  {{ participant.company }}
  </td>
  <td>
  {{ participant.country }}
  </td>
  <td>
  <a href="mailto:{{ participant.contact_email }}">{{ participant.contact_name }}</a>
  {% if participant.role == "Co-operating agent" %}
  <br/>
  {{ participant.role }}
  {% endif %}
  </td>
</tr>
{% endfor %}
</tbody>
</table>


