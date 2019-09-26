#!groovy
def parallel_steps = [:]

def createStep(stepClosures) {
	node() {
      stepClosures.each { k, v ->
        stage(k, v)
      }
	}
}

parallel_steps_with['Hello, Parallel World 1'] = {
  createStep([
    'Parallel World 1': {
     try {
      echo "Parallel World 1"
	  } finally {
        archiveArtifacts allowEmptyArchive: true, artifacts: 'test.log'
      }
    },
  ])
}

parallel_steps['Hello, Parallel World 2'] = {
  createStep([
    'Parallel World 2': {
     try {
      echo "Parallel World 2"
	  } finally {
        archiveArtifacts allowEmptyArchive: true, artifacts: 'test.log'
      }
    },
  ])
}

createStep([
	'Prepare Workspace': {
		checkout scm
	}
])

createStep([
	'Hello, World': {
		echo "Hello, World"
	}
])


parallel parallel_steps