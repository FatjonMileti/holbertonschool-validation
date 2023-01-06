build:  ## Builds a website using
	hugo
clean:  ## Cleans content from dist directory
	rm -rf ./dist
post:  ## Creates a new post using env variables POST_NAME and POST_TITLE
	hugo new posts/$(POST_NAME).md
	sed -i 's/title: .*/title: "$(POST_TITLE)"/g' ./content/posts/$(POST_NAME).md

help:  ## Show this help usage
	@fgrep -h "##" $(MAKEFILE_LIST) | fgrep -v fgrep | sed -e 's/\\$$//' | sed -e 's/##//'