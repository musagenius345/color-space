<script>
	/**
	 * @extends {"./ButtonSkeleton.svelte"} ButtonSkeletonProps
	 * @restProps {button | a | div}
	 * @slot {{ props: { role: "button"; type?: string; tabindex: any; disabled: boolean; href?: string; class: string; [key: string]: any; } }}
	 */

	/**
	 * Specify the kind of button
	 * @type {"primary" | "secondary" | "tertiary" | "ghost" | "danger" | "danger-tertiary" | "danger-ghost"}
	 */
	export let kind = 'primary';

	/**
	 * Specify the size of button
	 * @type {"default" | "field" | "small" | "lg" | "xl"}
	 */
	export let size = 'default';

	/** Set to `true` to use Carbon's expressive typesetting */
	export let expressive = false;

	/**
	 * Set to `true` to enable the selected state for an icon-only, ghost button
	 */
	export let isSelected = false;

	/**
	 * Specify the icon to render
	 * @type {typeof import("svelte").SvelteComponent}
	 */
	export let icon = undefined;

	/**
	 * Specify the ARIA label for the button icon
	 * @type {string}
	 */
	export let iconDescription = undefined;

	/** Set to `true` to disable the button */
	export let disabled = false;

	/**
	 * Set the `href` to use an anchor link
	 * @type {string}
	 */
	export let href = undefined;

	/** Specify the tabindex */
	export let tabindex = '0';

	/** Specify the `type` attribute for the button element */
	export let type = 'button';

	/** Obtain a reference to the HTML element */
	export let ref = null;

	$: hasIconOnly = icon && !$$slots.default;
	$: buttonProps = {
		type: href && !disabled ? undefined : type,
		tabindex,
		disabled: disabled === true ? true : undefined,
		href,
		'aria-pressed': hasIconOnly && kind === 'ghost' && !href ? isSelected : undefined,
		...$$restProps,
		class: [
			'btn',
			expressive && 'btn--expressive',
			((size === 'small' && !expressive) ||
				(size === 'sm' && !expressive) ||
				(size === 'small' && !expressive)) &&
				'btn--sm',
			(size === 'field' && !expressive) || (size === 'md' && !expressive && 'btn--md'),
			size === 'field' && 'btn--field',
			size === 'small' && 'btn--sm',
			size === 'lg' && 'btn--lg',
			size === 'xl' && 'btn--xl',
			kind && `btn--${kind}`,
			disabled && 'btn--disabled',
			hasIconOnly && 'btn--icon-only',
			$$restProps.class
		]
			.filter(Boolean)
			.join(' ')
	};
</script>

{#if href && !disabled}
	<!-- svelte-ignore a11y-missing-attribute -->
	<a bind:this={ref} {...buttonProps}>
		{#if hasIconOnly}
			<span class:assistive-text={true}>{iconDescription}</span>
		{/if}
		<slot /><svelte:component
			this={icon}
			aria-hidden="true"
			class="btn__icon"
			aria-label={iconDescription}
		/>
	</a>
{:else}
	<button bind:this={ref} {...buttonProps} on:click on:mouseover on:mouseenter on:mouseleave>
		{#if hasIconOnly}
			<span class:assistive-text={true}>{iconDescription}</span>
		{/if}
		<slot /><svelte:component
			this={icon}
			aria-hidden="true"
			class="btn__icon"
			style={hasIconOnly ? 'margin-left: 0' : undefined}
			aria-label={iconDescription}
		/>
	</button>
{/if}

<style>
	.btn {
		overflow: hidden;
		height: 2rem;
	}

	.btn {
		font-size: var(--font-size, 0.875rem);
		font-weight: var(--font-weight, 400);
		line-height: var(--line-height, 1.28572);
		letter-spacing: var(--letter-spacing, 0.16px);
		position: relative;
		display: inline-flex;
		max-width: 20rem;
		min-height: 3rem;
		flex-shrink: 0;
		align-items: center;
		justify-content: space-between;
		padding: calc(0.875rem - 3px) 63px calc(0.875rem - 3px) 15px;
		margin: 0;
		border-radius: 0.3rem;
		cursor: pointer;
		outline: none;
		text-align: center;
		text-decoration: none;
		transition: background 70ms cubic-bezier(0, 0, 0.38, 0.9),
			box-shadow 70ms cubic-bezier(0, 0, 0.38, 0.9), border-color 70ms cubic-bezier(0, 0, 0.38, 0.9),
			outline 70ms cubic-bezier(0, 0, 0.38, 0.9);
		vertical-align: top;
	}

	.btn:disabled,
	.btn:hover:disabled,
	.btn:focus:disabled,
	.btn.btn--disabled,
	.btn.btn--disabled:hover,
	.btn.btn--disabled:focus {
		border-color: var(--disabled-02, #c6c6c6);
		background: var(--disabled-02, #c6c6c6);
		box-shadow: none;
		color: var(--disabled-03, #8d8d8d);
		cursor: not-allowed;
	}

	.btn .btn__icon {
		position: absolute;
		right: 1rem;
		width: 1rem;
		height: 1rem;
		flex-shrink: 0;
	}

	.btn::-moz-focus-inner {
		padding: 0;
		border: 0;
	}

	.btn--primary {
		border-width: 1px;
		border-style: solid;
		border-color: rgba(0, 0, 0, 0);
		background-color: var(--accent, #0f62fe);
		color: var(--txt, #ffffff);
	}

	.btn--primary:hover {
		background-color: var(--hover-primary, #0353e9);
	}

	.btn--primary:focus {
		border-color: var(--focus, #0f62fe);
		box-shadow: inset 0 0 0 1px var(--focus, #0f62fe), inset 0 0 0 2px var(--ui-background, #ffffff);
	}

	.btn--primary:active {
		background-color: var(--active-primary, #002d9c);
	}

	.btn--primary .btn__icon,
	.btn--primary .btn__icon path:not([data-icon-path]):not([fill='none']) {
		fill: currentColor;
	}

	.btn--primary:hover {
		color: var(--text-04, #ffffff);
	}

	.btn--secondary {
		border-width: 1px;
		border-style: solid;
		border-color: rgba(0, 0, 0, 0);
		background-color: var(--interactive-02, #393939);
		color: var(--text-04, #ffffff);
	}

	.btn--secondary:hover {
		background-color: var(--hover-secondary, #4c4c4c);
	}

	.btn--secondary:focus {
		border-color: var(--focus, #0f62fe);
		box-shadow: inset 0 0 0 1px var(--focus, #0f62fe), inset 0 0 0 2px var(--ui-background, #ffffff);
	}

	.btn--secondary:active {
		background-color: var(--active-secondary, #6f6f6f);
	}

	.btn--secondary .btn__icon,
	.btn--secondary .btn__icon path:not([data-icon-path]):not([fill='none']) {
		fill: currentColor;
	}

	.btn--secondary:hover,
	.btn--secondary:focus {
		color: var(--text-04, #ffffff);
	}

	.btn--tertiary {
		border-width: 1px;
		border-style: solid;
		border-color: var(--interactive-03, #0f62fe);
		background-color: rgba(0, 0, 0, 0);
		color: var(--interactive-03, #0f62fe);
	}

	.btn--tertiary:hover {
		background-color: var(--hover-tertiary, #0353e9);
	}

	.btn--tertiary:focus {
		border-color: var(--focus, #0f62fe);
		box-shadow: inset 0 0 0 1px var(--focus, #0f62fe), inset 0 0 0 2px var(--ui-background, #ffffff);
	}

	.btn--tertiary:active {
		background-color: var(--active-tertiary, #002d9c);
	}

	.btn--tertiary .btn__icon,
	.btn--tertiary .btn__icon path:not([data-icon-path]):not([fill='none']) {
		fill: currentColor;
	}

	.btn--tertiary:hover {
		color: var(--inverse-01, #ffffff);
	}

	.btn--tertiary:focus {
		background-color: var(--interactive-03, #0f62fe);
		color: var(--inverse-01, #ffffff);
	}

	.btn--tertiary:active {
		border-color: rgba(0, 0, 0, 0);
		background-color: var(--active-tertiary, #002d9c);
		color: var(--inverse-01, #ffffff);
	}

	.btn--tertiary:disabled,
	.btn--tertiary:hover:disabled,
	.btn--tertiary:focus:disabled,
	.btn--tertiary.btn--disabled,
	.btn--tertiary.btn--disabled:hover,
	.btn--tertiary.btn--disabled:focus {
		background: rgba(0, 0, 0, 0);
		color: var(--disabled-03, #8d8d8d);
		outline: none;
	}

	.btn--sm {
		min-height: 2rem;
		padding: calc(0.375rem - 3px) 60px calc(0.375rem - 3px) 12px;
	}

	.btn--xl:not(.btn--icon-only) {
		align-items: baseline;
		padding-top: var(--spacing-05, 1rem);
		padding-right: var(--spacing-10, 4rem);
		padding-left: var(--spacing-05, 1rem);
		min-height: 5rem;
	}

	.btn--lg:not(.btn--icon-only) {
		align-items: baseline;
		padding-top: var(--spacing-05, 1rem);
		padding-right: var(--spacing-10, 4rem);
		padding-left: var(--spacing-05, 1rem);
		min-height: 4rem;
	}

	.btn--field,
	.btn--md {
		min-height: 2.5rem;
		padding: calc(0.675rem - 3px) 60px calc(0.675rem - 3px) 12px;
	}

	.btn--expressive {
		font-size: var(--font-size, 1rem);
		font-weight: var(--font-weight, 400);
		line-height: var(--line-height, 1.375);
		letter-spacing: var(--letter-spacing, 0);
		min-height: 3rem;
	}

	.btn--icon-only.btn--expressive {
		padding: 12px 13px;
	}

	.btn.btn--expressive .btn__icon {
		width: 1.25rem;
		height: 1.25rem;
	}
</style>
