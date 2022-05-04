<script lang="ts">
    import { onMount } from 'svelte';
    import OpenSeadragon from 'openseadragon'

    export let width:string
    export let height:string
    export let url:string

    onMount(() => {
        let viewer = OpenSeadragon({
                id: "test1",
                prefixUrl: "/node_modules/openseadragon/build/openseadragon/images/",
                preserveViewport: true,
                showNavigator:  true,
                toolbar: "toolbarDiv",
                visibilityRatio:    1,
                minZoomLevel:       1,
                defaultZoomLevel:   1,
                sequenceMode:       true,
                tileSources:   [{                                                               
                    "@context": "http://iiif.io/api/image/2/context.json",
                    "@id": url,
                    "height": 7200,
                    "width": 5233,
                    "profile": [ "http://iiif.io/api/image/2/level2.json" ],
                    "protocol": "http://iiif.io/api/image",
                    "tiles": [{
                        "scaleFactors": [ 1, 2, 4, 8, 16, 32 ],
                        "width": 1024
                    }]                  
                }]
            })
    })


</script>

<div id="toolbarDiv"></div>

<div id="test1" style="width: {width}px; height: {height}px;"></div>
