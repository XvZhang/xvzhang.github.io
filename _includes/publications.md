<h1 id="publications"></h1>

<h2 style="margin: 30px 0px -15px;">Publications <temp style="font-size:15px;">[</temp><a href="https://scholar.google.com/citations?user=sf-0AGoAAAAJ&hl=de" target="_blank" style="font-size:15px;">Google Scholar</a><temp style="font-size:15px;">]</temp></h2>

<div class="publications">

{% for publication in site.data.publications.main %}
<li style="list-style-type: none; margin-bottom: 8px;">

<div class="pub-entry">
  <div style="display: flex; align-items: center; flex-wrap: wrap; margin-bottom: 5px;">
    <div class="title" style="flex-grow: 1; min-width: 0;">
      {% if publication.pdf %}
        <a href="{{ publication.pdf }}" target="_blank">{{ publication.title }}</a>
      {% else %}
        {{ publication.title }}
      {% endif %}
    </div>
    <div class="conference" style="margin-right: 10px;"><em>{{ publication.conference }}</em></div>
    {% if publication.pdf %}
      <a href="{{ publication.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="color:#0404B4; font-size:18px; margin-right: 10px;">PDF</a>
    {% endif %}
    {% if publication.notes %}
      <strong><i style="color:#e74d3c;">{{ publication.notes }}</i></strong>
    {% endif %}
  </div>
  <div class="author" style="margin-top: 5px;">{{ publication.authors }}</div>
</div>
</li>

{% endfor %}
</div>


