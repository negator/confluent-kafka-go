load("@io_bazel_rules_go//go:def.bzl", "cgo_library", "go_prefix")

go_prefix("github.com/confluentinc/confluent-kafka-go/kafka")

licenses(["notice"])

cc_library(
	name = "glue",
	hdrs = ["glue_rdkafka.h"],	
	includes = ["."],	
)

cgo_library (
	name = "default_cgo_library",
	srcs = glob(
		include = ["]*"], 
		exclude = [
			"**/README",
			"**/*.html",
			"**/.gitignore",
			"**/*.json",			
			"**/*_test.go", 			
		]
	),
	copts = ["-I","."],
	cdeps = [
		"@com_github_edenhill_librdkafka//:librdkafka", 
		":glue"		
	],
	visibility = ["//visibility:public"],
)

