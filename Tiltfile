local_resource(
	labels=["build"],
	name="lualatex",
	cmd=[
		# Entrypoint
		"lualatex",
		# Options 
		"--halt-on-error",
		"--interaction=nonstopmode",
		"--jobname=resume",
		"--output-directory=../build",
		"--output-format=pdf",
		"--shell-escape",
		# Input arguments
		"main.tex",
	],
	dir="source",
	deps=[
		"assets/",
		"source/main.tex"
	],
)

local_resource(
	labels=["viewer"],
	name="preview",
	cmd="open build/resume.pdf",
	deps=[],
	resource_deps=["lualatex"],
)
