<script lang="ts">
	import { Menubar } from "bits-ui";

	let view = "table";
</script>

<Menubar.Root
	class="flex h-12 items-center gap-1 rounded-10px border border-dark-10 bg-background-alt px-[3px] shadow-mini"
>
	<Menubar.Menu>
		<Menubar.Trigger
			class="inline-flex h-10 cursor-default items-center justify-center rounded-9px px-3 text-sm font-medium !ring-0 !ring-transparent data-[highlighted]:bg-muted data-[state=open]:bg-muted"
			>View</Menubar.Trigger
		>
		<Menubar.Content
			class="z-50 w-full max-w-[220px] rounded-xl border border-muted bg-background px-1 py-1.5 shadow-popover !ring-0 !ring-transparent "
			align="start"
			sideOffset={3}
		>
			<Menubar.RadioGroup bind:value={view}>
				<Menubar.RadioItem
					value="table"
					class="flex h-10 select-none items-center rounded-button py-3 pl-3 pr-1.5 text-sm font-medium !ring-0 !ring-transparent data-[highlighted]:bg-muted"
				>
					Table
					<Menubar.RadioIndicator class="ml-auto">✅</Menubar.RadioIndicator>
				</Menubar.RadioItem>
				<Menubar.RadioItem
					value="board"
					class="flex h-10 select-none items-center rounded-button py-3 pl-3 pr-1.5 text-sm font-medium !ring-0 !ring-transparent data-[highlighted]:bg-muted"
				>
					Board
					<Menubar.RadioIndicator class="ml-auto">✅</Menubar.RadioIndicator>
				</Menubar.RadioItem>
				<Menubar.RadioItem
					value="gallery"
					class="flex h-10 select-none items-center rounded-button py-3 pl-3 pr-1.5 text-sm font-medium !ring-0 !ring-transparent data-[highlighted]:bg-muted"
				>
					Gallery
					<Menubar.RadioIndicator class="ml-auto">✅</Menubar.RadioIndicator>
				</Menubar.RadioItem>
			</Menubar.RadioGroup>
		</Menubar.Content>
	</Menubar.Menu>
</Menubar.Root>
