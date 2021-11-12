pipeline 

{

	agent any

		Stages {


					Stage ('Step One')	

						{

							steps { 
									echo "This is Step One"

							   	}


						}

					Stage ('Step Two')	

						{

							steps { 
									input ("Do you want to proceed?")

							   	}


						}


					Stage ('Step Three')	

						{

							when {
								not {

									branch 'master'
								}


							}

							steps { 
									echo "This is Step Three"

							   	}


						}

					Stage ('Step Four')	

						{

							parallel {


								Stage ('Unit Test')	

										{

											steps { 
													echo "This is Unit Test Stage"

											   	}


										}	


								Stage ('Integration Test')	

								{


									agent {

										docker {

											reuseNode false
											image 'ubuntu'

												}	

											}


									steps { 
											echo "This is Integration Test Stage"

									   	}


								}	




							}




						}



				}

}
