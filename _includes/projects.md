<style>

/* Apply shadow to odd-numbered entries */
.pub-entry:nth-child(odd) {
  box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1); /* Example shadow */
  padding: 15px;
  margin-bottom: 30px;
  background-color: white; /* Optional: if you want to have a colored background */
}

/* Apply no shadow to even-numbered entries */
.pub-entry:nth-child(even) {
  box-shadow: none;
  padding: 15px;
  margin-bottom: 30px;
}

</style>

<h1 id="projects"></h1>

<h2 style="margin: 30px 0px -15px;">Experiences <temp style="font-size:15px;"></temp></h2>

<div class="publications">

{% for project in site.data.projects.main %}
<li style="list-style-type: none; margin-bottom: 8px;">

<div class="pub-entry">
  <div class="title" style="margin-top: 5px;"><strong>{{ project.title }}</strong></div>
  <div style="margin-top: 5px;">
    <span class="school">{{ project.school }}</span> |
    <span class="dates"><em>{{ project.dates }}</em></span>
  </div>
  <div class="projects" style="margin-top: 5px;">
    {% for item in project.projects %}
    <div>• {{ item }}</div>
    {% endfor %}
  </div>
</div>
</li>

{% endfor %}
</div>

