pipeline 

{

	agent any

		stages {


					stage ('Step One')	

						{

							steps { 
									echo "This is Step One"

							   	}


						}

					stage ('Step Two')	

						{

							steps { 
									input ("Do you want to proceed?")

							   	}


						}


					stage ('Step Three')	

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

					stage ('Step Four')	

						{

							parallel {


								stage ('Unit Test')	

										{

											steps { 
													echo "This is Unit Test Stage"

											   	}


										}	


								stage ('Integration Test')	

								{


									agent any


									steps { 
											echo "This is Integration Test Stage"

									   	}


								}	




							}




						}



				}

}
