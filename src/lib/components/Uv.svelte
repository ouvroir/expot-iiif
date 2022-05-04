<script>
      
    
    
    var urlAdaptor = new UV.URLAdaptor();

      const data = urlAdaptor.getInitialData({
        manifest: "https://wellcomelibrary.org/iiif/b18035723/manifest",
        embedded: true // needed for codesandbox frame
      });

      uv = UV.init("uv", data);
      urlAdaptor.bindTo(uv);
    </script>
<div class="uv" id="uv"></div>




<style>
    #uv {
      width: 1800px;
      height: 958px;
    }
  </style>