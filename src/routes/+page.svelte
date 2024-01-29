<script>
    import { fns, AppShell, Navbar, Header, Title, Divider, Center, Container } from '@svelteuidev/core';
    import Main from '../pages/Main.svelte'

    let isDark = false;
    let opened = false;

    function toggleTheme() {
        isDark = !isDark;
    }
    function toggleOpened() {
        opened = !opened;
    }
</script>

<AppShell>
    <Header height="20" slot="header">
        <Center>
            <Title>Wavvle</Title>
        </Center>
    </Header>

    <Container>
        <Main />
    </Container>
</AppShell>