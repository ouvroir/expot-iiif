<script lang="ts">
    import OsdViewer from '/src/lib/components/OsdViewer.svelte'

</script>
<h1>Test composant OpenSeadragon</h1>

<p>composant svelte avec paramètre de hauteur, largeur et url</p>

<OsdViewer 
    url="https://libimages1.princeton.edu/loris/pudl0001%2F4609321%2Fs42%2F00000001.jp2"
    height="600" width="600"
/>