<div class="row">
  <div class="medium-12 columns">
    <h3>Upcoming Workshops from INCLUDES</h3>
    <table class="table table-striped workshops"  style="width: 100%;">
      {% for w in site.data.swc_upcoming_workshops %}
      <tr>
    <td>
      <img src="{{site.filesurl}}/flags/{{site.flag_size}}/{{w.country | downcase}}.png" title="{{w.country | replace: '-', ' '}}" alt="{{w.country | replace: '-', ' ' | downcase}}" />
      <a href="{{w.url}}">{{w.venue}}</a>
          <br/>
      {{w.start_date | date: "%b %-d"}} - {{w.end_date | date: "%b %-d, %Y"}}
          {% if w.instructors %}
          <br/>
          <b>Instructors:</b> {{ w.instructors | replace: ",", ", "}}
          {% endif %}
          {% if w.helpers %}
          <br/>
          <b>Helpers:</b> {{ w.helpers  | replace: ",", ", "}}
          {% endif %}
    </td>
      </tr>
      {% endfor %}
      <tr>
    <td>
      <em><a href="{{site.baseurl}}/workshops/">See more...</a></em>
    </td>
      </tr>
    </table>
  </div>
</div><!--end of row-->