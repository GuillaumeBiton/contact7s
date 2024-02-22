<script>
    import { Navbar, Page, List, ListGroup, ListItem, Block } from 'framework7-svelte';

    export let contactsList;
/*    let contactsList = [
        {
            groupTitle : 'A',
            groupItems: [
                {
                    title: 'Aaron',
                },
                {
                    title: 'Abbie',
                },
            ],
        },
        {
            groupTitle: 'B',
            groupItems: [
                {
                    title: 'Bernard',
                },
                {
                    title: 'Bob',
                },
            ]
        },
        {
            groupTitle: 'C',
            groupItems: [
                {
                    title: 'Bernard',
                },
                {
                    title: 'Bob',
                },
            ]
        },
        {
            groupTitle: 'D',
            groupItems: [
                {
                    title: 'Bernard',
                },
                {
                    title: 'Bob',
                },
            ]
        },
        {
            groupTitle: 'E',
            groupItems: [
                {
                    title: 'Bernard',
                },
                {
                    title: 'Bob',
                },
            ]
        },
        {
            groupTitle: 'F',
            groupItems: [
                {
                    title: 'Bernard',
                },
                {
                    title: 'Bob',
                },
            ]
        },
        {
            groupTitle: 'G',
            groupItems: [
                {
                    title: 'Bernard',
                },
                {
                    title: 'Bob',
                },
            ]
        },
    ];
*/    
</script>

<Page>
    <Navbar title="contacts"></Navbar>
    {#if contactsList}
    <List contactsList ul={false} strongIos>
        <ListGroup>
            {#each contactsList as group}
            <ListItem title={group.groupTitle} groupTitle />
            {#each group.groupItems as contact}
            <ListItem title={contact.title} />
            {/each}
            {/each}
        </ListGroup>
    </List>
    {:else}
    <Block strong outline inset><p>contacts list is empty</p></Block>
    {/if}
</Page>