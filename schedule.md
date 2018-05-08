---
layout: default
title: Schedule & Material 
---

Links to the course material will be provided in the schedule below
after each class.
You may want to have a look at the
[previous edition of the course](http://coltekin.net/cagri/courses/snlp2017/)
for reference.


## Reading material
- Daniel Jurafsky and James H. Martin (2009)
  _Speech and Language Processing:
   An Introduction to Natural Language Processing,
   Computational Linguistics, and Speech Recognition_.
   Pearson Prentice Hall, second edition (**JM**)
   [chapters from 3rd edition draft](http://web.stanford.edu/~jurafsky/slp3/)
   (**JM3**)
- Trevor Hastie, Robert Tibshirani, and Jerome Friedman (2009),
  _The Elements of Statistical Learning:
   Data Mining, Inference, and Prediction_.
   Springer-Verlag, second edition. (**HTF**)
   [available online](http://web.stanford.edu/~hastie/ElemStatLearn/)


## The course schedule

<table rules="groups" style="width:100%;border-collapse: collapse;">
  <thead style="border-bottom: 1px solid #000;">
    <tr>
      <th style="text-align:left;" width="10%">Week</th>
      <th style="text-align:left;" width="30%">Monday</th>
      <th style="text-align:left;" width="30%">Wednesday</th>
      <th style="text-align:left;" width="30%">Friday</th>
    </tr>
  </thead>
  <tbody style="border-bottom: 1px solid #000;">
{% for week in site.data.schedule %}
    <tr style="border-bottom: 1px solid #000;">
    <td style="text-align:left;"> {{ week.week }} </td>
    {% for date in week.dates %}
            <td valign="top"> {{ date[0] }} <br/>
                {% if date[1].topic %}
                    {{ date[1].topic }}&nbsp;
                {% else %}
                    <em style="color: red">No class</em>
                {% endif %}
                {% if date[1].links %}
                    <br/>
                    [{% for link in date[1].links %}<a href="{{ link[1] }}">{{ link[0] }}</a>{% unless forloop.last %}, {% endunless %}{% endfor %}]
                {% endif %}
                {% if date[1].reading %}
                    <br/>
                    Reading: {{ date[1].reading }}
                {% endif %}
            </td>
    {% endfor %}
    </tr>
{% endfor %}
  </tbody>
</table>
