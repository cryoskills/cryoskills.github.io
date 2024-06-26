---
title: Course Details - Norway
banner_image: /assets/img/course2024/sensors_outside_jenkins_samantha.jpg
---
<div class="alert alert-warning container" role="alert">
    This information is available as <strong>a guide only</strong> - course content, location and timings may change for future courses.
</div>

<div class="my-5 container text-left">
    <div class="row">
        <!--- Course Location -->
        <section class="col-lg-4 order-lg-last">
          <h1>Course Venue</h1>
          <p>
              <strong>Haugastøl Turistcenter.</strong>, Haugastøl, Norway
          </p>
          <p>
              <strong>Website:</strong> <a href="https://www.haugastol.no/en">https://www.haugastol.no/en</a>
          </p>
          <div id="map" style="height: 200px"></div>
      </section>

      <div class="col-lg-8 order-lg-first my-3 my-lg-0">

        {% capture about_content %}{% include about/haugastol_2024.md %}{% endcapture %}
        {{ about_content | markdownify }}
        
      </div>

    </div>
  </div>

<!--- Load Leaflet Map for Course Venue -->
<script>
    $(document).ready(function () {

    console.log("Loading Inner Hebrides Map")

    // Get OSM Tlles
    var osm_map = L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
        maxZoom: 19,
        attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
    });

    var map_layers = {}

    // Load Map Object
    var map = L.map('map', {
        layers : [osm_map]
    }).setView([60.512504, 7.852631], 12);

    // Option
    var marker = new L.Marker([60.512504, 7.852631]);
    marker.addTo(map);

    console.log({"OSM":osm_map})
    console.log(map_layers)

    });
</script>