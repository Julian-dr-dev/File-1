# File-1
Library-video store project.

class Dvd {
  constructor(title) {
    this._title = title;
    this._releaseDate = releaseDate;
    this._isCheckedOut = false;
  }
  get title() {
    return this._title;
  }
  get runTime() {
    return this._runTime;
  }
  get isCheckedOut() {
    return this._isCheckedOut;
  }
   isCheckedOut(value) {
    return this._isCheckedOut = value;
  }
  toggleCheckOutStatus() {
    this.isCheckedOut = !this.isCheckedOut;
  }
   getAverageRating() {
  let ratingsSum = this.ratings.reduce((accumulator, rating) => accumulator + rating);
  return ratingsSum / this.ratings.length
  }

  addRating(value) {
    this.ratings.push(value);
  }
}

class documentary extends Dvd {
  constructor(subject, title) {
    super(title);
    this._subject = subject;
  }
  get subject() {
    return this._subject;
  }
}
class Feature extends Dvd {
  constructor(director, title, runTime, genre) {
    super(title);
    this._director = director;
    this._runTime = runTime;
    this._genre = genre;
  }
  get director() {
    return this._director;
  }
  get runTime() {
    return this._runTime;
  }
  get genre() {
    return this._genre;
  }
}

class workOutVideo extends Dvd {
  constructor(host, title, workoutType) {
    super(title);
    this._host = host;
    this._workoutType = workoutType;
  }
  get host() {
    return this._host;
  }
  get workoutType() {
    return this._workoutType;  
  }
}

class tvSeriesDvd extends Dvd {
  constructor(seasonNumber, title, episodeCount) {
    super(title);
    this._seasonNumber = seasonNumber;
    this._episodeCount = episodeCount;
   }
   get seasonNumber() {
    return this._seasonNumber;
   }
   get episodeCount() {
    return this._episodeCount;
   }
 }

const theScheme = new documentary('Sports Scandal', 'The Scheme');
theScheme.toggleCheckOutStatus();
console.log(theScheme.isCheckedOut);

theScheme.addRating(9);
theScheme.addRating(10);
theScheme.addRating(8.5);

theScheme.getAverageRating();


const Casino = new Feature('Martin Scorcese', 'Casino','178', crime);
Casino.toggleCheckOutStatus();
console.log(Casino.isCheckedOut);

Casino.addRating(9)
Casino.addRating(10)
Casino.addRating(8.5)

Casino.getAverageRating();


const brazilButtLift = new workOutVideo
brazilButtLift.toggleCheckOutStatus();
console.log(brazilButtLift.isCheckedOut);

brazilButtLift.addRating(6)
brazilButtLift.addRating(5)
brazilButtLift.addRating(9.5)

brazilButtLift.getAverageRating();

