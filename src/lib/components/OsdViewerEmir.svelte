<script lang="ts">
    import { onMount } from 'svelte';
    import OpenSeadragon from 'openseadragon'

   
 


    onMount(() => {
        let viewer = OpenSeadragon({
                id: "test1",
                prefixUrl: "/node_modules/openseadragon/build/openseadragon/images/",
                preserveViewport: true,
                visibilityRatio:    1,
                minZoomLevel:       1,
                defaultZoomLevel:   1,
                sequenceMode:       true,
                tileSources: [ "https://cdm22028.contentdm.oclc.org/iiif/2/baby:25198/info.json",
                "https://libimages1.princeton.edu/loris/pudl0001%2F4609321%2Fs42%2F00000001.jp2/info.json"
                ]                                            
                
            })
    })


</script>

<div id="test1"  style="width: 500px; height: 450px"></div>