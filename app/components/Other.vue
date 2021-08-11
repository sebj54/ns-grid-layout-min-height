<template>
    <Page>
        <ActionBar>
            <Label text="Other"/>
        </ActionBar>

        <StackLayout>
            <GridLayout backgroundColor="blue" minHeight="300">
                <StackLayout>
                    <Label class="info" backgroundColor="green">
                        <FormattedString>
                            <Span class="fas" text.decode="&#xf135; "/>
                            <Span text="GridLayout + min-height"/>
                        </FormattedString>
                    </Label>

                    <Button
                        class="btn"
                        text="View GridLayout in ScrollView"
                        @tap="goToHomePage"
                    />
                </StackLayout>
            </GridLayout>
        </StackLayout>
    </Page>
</template>

<script>
import Home from './Home'

export default {
    methods: {
        goToHomePage() {
            this.$navigateTo(Home)
        },
    },
};
</script>

<style scoped lang="scss">
    @import '@nativescript/theme/scss/variables/blue';

    // Custom styles
    .fas {
        @include colorize($color: accent);
    }

    .info {
        font-size: 20;
        horizontal-align: center;
        vertical-align: center;
    }
</style>
