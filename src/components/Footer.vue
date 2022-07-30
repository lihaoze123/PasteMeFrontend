<template>
    <div class="row">
        <div class="col-md-12">
            <div class="footer">
                <p>
                    <a href='http://www.chumeng.me' target='_blank'>Chumeng's Blog</a>
                    <a v-for="footer in $store.state.config.footer" v-bind:key="footer.id">&nbsp;&nbsp;|&nbsp;&nbsp;<a
                            :href="footer.url" target="_blank">{{ footer.text }}</a></a>
                </p>
                <p>
                    <a>Copyright&nbsp;&copy;&nbsp;2022&nbsp;-&nbsp;{{ year }}&nbsp;</a>
                </p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Footer",
    data() {
        return { year: new Date().getFullYear(), }
    }
}
</script>

<style scoped>
.footer {
    font-size: .8em;
    text-align: center;
}

.footer p {
    margin: 1em;
}

.footer a:link,
.footer a:visited {
    color: #38488f;
}

.logo img {
    height: 2em;
}

.logo svg {
    height: 2em;
}

.logo {
    margin: .5em;
}
</style>
