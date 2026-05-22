.DEFAULT_GOAL := help

SRCS = ./index.html ./styles.css

help:
	@echo
	@echo -e "jayshozie.github.io Repo - My Resume"
	@echo -e "Options:"
	@echo -e "  help       Print this message"
	@echo -e "  install    Install dependencies via 'bundle install'"
	@echo -e "  test       Deploy the website locally on port 4000"
	@echo -e "  deploy     Wrapper for 'git add . ; git commit -s'"

install:
	bundle install

test: $(SRCS)
	bundle exec jekyll serve || exit 1 \
	# @if ! command bundle > /dev/null 2>&1; then \
	# 	@echo -e "[ERR] Bundler not found!" \
	# else \
	# fi

deploy: $(SRCS)
	git add .
	git commit -s

.PHONY = help test deploy
