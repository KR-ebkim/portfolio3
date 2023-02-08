<template>
	<v-card to="/products">
test

	</v-card>
</template>

<script setup>
	const email = ref("");
	const password = ref("");

	const { ruleEmail, rulePassLen, ruleRequired } = useFormRules();

	const submit = async () => {};
</script>
