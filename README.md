# Assignment-2

## Put comments here that give an overall description of what your
## functions do
      ## Well, as the tasks state, my functions will do the following:
      ## Make a cache matrix that can invert itself
      ## Inverse the inversed cache, unless it's not inversed

## Write a short comment describing this function
      ##set the value of the matrix
      ##get the value of the matrix
      ##set the value of the inverse
      ##get the value of the inverse

makeCacheMatrix <- function(x = matrix()) {
      m <- NULL
      set <- function(y) {
            
      x <<- y
      m <<- NULL
      }
      get <- function() x
      setmatrix <- function(solve) m <<- solve
      getmatrix <- function() m
      list(set = set, get = get,
           setmatrix = setmatrix)
           getmatrix = getmatrix
}


## Write a short comment describing this function
## Retrieving information from the former setup if available, otherwise finding
## it through the last piece of code starting with "data"

cacheSolve <- function(x, ...) {
      m <- x$getmatrix()
      if(!is.null(m)) {
            return(m)
      }
      data <- x$get()
      m <- solve(data,...)
      x$setmatrix(m)
      m
}

