#<test id> = {
#	year = <year>   #the start year when the test is started to be checked
#	success = {
#		<triggers>  #the triggers the test need to fulfill for it to pass
#	}
#	failure = {
#		<triggers>  #the triggers the test need to fulfill for it to fail
#	}
#	end_year = <year>   #the test will be inactive once this year is passed
#	fail_on_end_year = <yes/no> #the test will automatically fail if that date passes if set to yes, defaults to no
#	success_effect = {
#		<effects>   #effects which happen if the test passes, make sure to only use test_log though
#	}
#	failure_effect = {
#		<effects>   #effects which happen if the test passes, make sure to only use test_log though
#	}
#}