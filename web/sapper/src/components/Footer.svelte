<script>
    /**
     * Footer component for main page
     */

    // GUI components imports
    import Col from 'sveltestrap/src/Col.svelte'
    import Container from 'sveltestrap/src/Container.svelte'
    import Row  from "sveltestrap/src/Row.svelte"

    // Data for footer
    let header = "goTemp";
    let osTechList = ["GO", "go-Micro", "Svelte", "NATS"];
    let dbTechList = ["ArangoDB", "PostgreSQL", "Redis", "TimescaleDB"];
    let description = "This project provides a sample microservices implementation. goTemp was built by Juan Peredo at ";
    let bolbeck = {label:"Bobleck.com", address: "https://www.bolbeck.com"}

</script>

<style>

    footer {
        position: fixed;
        left: 0;
        bottom: 0;
        height: 150px;
        width: 100%;
        overflow: hidden;
    }

</style>

<footer class="p-3 my-3 bg-light">

    <Container>
        <Row>
            <Col></Col>
            <Col class="col-4">
                <h6>{header}</h6>
                <p>
                    {description}<a href="{bolbeck.address}">{bolbeck.label}</a>
                </p>
            </Col>
            <Col class="col-3">
                <h6>Powered by open source</h6>
                <ul class="list-unstyled">
                    {#each osTechList as list}
                        <li>{list}</li>
                    {/each}
                </ul>
            </Col>
            <Col class="col-3">
                <h6>Powered by open source DBs</h6>
                <ul class="list-unstyled">
                    {#each dbTechList as list}
                        <li>{list}</li>
                    {/each}
                </ul>
            </Col>
            <Col></Col>
        </Row>
    </Container>
</footer>



