<script>
	import { _ } from 'svelte-i18n';

	import { Avatar, Card, CardActions, ProgressLinear } from 'svelte-materialify';
	import { progress } from './data';
</script>

<Card style="min-height: 120px;">
	<div class="card-top">
		<div class="pl-4 pr-4 pt-3">
			<span class="text-subtitle-2 grey-text text-darken-2"
				>{$_('app.dashboard.tasksProgress')}</span
			>
			<br />
			<span class="text-h5 mb-2">{$progress.value}%</span>
			<br />
		</div>
		<div class="icon">
			<Avatar size="50px" class="orange white-text">
				<span class="material-icons">group</span>
			</Avatar>
		</div>
	</div>
	<CardActions>
		<ProgressLinear value={$progress.value} style="margin: 1rem 0 0 0;" />
	</CardActions>
</Card>

<style>
	.card-top {
		display: flex;
		justify-content: space-between;
	}
	.card-top > .icon:last-child {
		margin-top: 1rem;
		margin-right: 1rem;
	}
</style>
