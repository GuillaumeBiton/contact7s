<script>
    import { Navbar, Page, List, ListGroup, ListItem, Block } from 'framework7-svelte';
    
    export let contactId;
    export let contact = {
        title: contactId,
    };
</script>

<Page name="contact">
    <Navbar title={contact.title} backLink></Navbar>
</Page>