<template>
    <Page>
        <ActionBar>
            <Label text="Home"/>
        </ActionBar>

        <GridLayout>
            <ScrollView>
                <GridLayout backgroundColor="blue">
                    <StackLayout>
                        <Label class="info" backgroundColor="green">
                            <FormattedString>
                                <Span class="fas" text.decode="&#xf135; "/>
                                <Span text="GridLayout in ScrollView"/>
                            </FormattedString>
                        </Label>

                        <Button
                            class="btn"
                            text="View GridLayout + min-height"
                            @tap="goToOtherPage"
                        />
                    </StackLayout>
                </GridLayout>
            </ScrollView>
        </GridLayout>
    </Page>
</template>

<script>
import Other from './Other'

export default {
    methods: {
        goToOtherPage() {
            this.$navigateTo(Other)
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
