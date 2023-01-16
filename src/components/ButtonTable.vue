<script>

import LinkButton from './LinkButton.vue';

    export default{
    data() {
        return {
            helloworld: "hello world",
            items:[ 
                {title:"SharePoint A IT EA -Simulation",desp:"The sharepoint"},
                {title:"ConNext - PSpice",desp:"what ever"},
                {title:"eLearning (TTKF)",desp:"videos"},
                {title:"Training Portal"},
                {title:"external: Community - News"},
                {title:"external: PSpice.com"},

            ],
        manualItems:[
            {title:"What's New"},
            {title:"Manual - Capture"},
            {title:"Manual - Conti Environment"},
            {title:"Manual - PSpice"},
            {title:"Manual - PSpice/MATLAB"},
            {title:"Documents - All"},
        ],
        modelsItems:[
            {title:"PSpice Updater"},
            {title:"Models - search (Excel)"},
            {title:"Models - search (MS Access DB)"},
            {title:"Models - search (LibraryBrowser)"},
            {title:"Models - Request (new,update,...)"},
            {title:"Models - Verification"},
        ]
        };
    },
    components: { LinkButton }
}
</script>

<template>
    <!-- <div>{{ helloworld }}</div> -->
    <section class="bg-dark text-light">
        <div class="container">
            <div class="d-md-flex align-items-center">
                    <div class="row">
                        <div class="col-md">
                            <ul class="list-goup list-group-flush lead">
                                <LinkButton :datas="items" strap_class="card-body list-group-item list-group-item-action bg-primary-subtle"></LinkButton>
                            </ul>
                        </div>
                        <div class="col-md">
                            <ul class="list-goup list-group-flush lead">

                                <LinkButton :datas="manualItems" strap_class="card-body list-group-item list-group-item-action list-group-item-secondary"></LinkButton>
                            </ul>
                        </div>
                        <div class="col-md">
                            <ul class="list-goup list-group-flush lead">

                                <LinkButton :datas="modelsItems" strap_class="card-body list-group-item list-group-item-action list-group-item-warning"></LinkButton>
                            </ul>
                        </div>
                    </div>
            </div>
        </div>

    </section>
</template>