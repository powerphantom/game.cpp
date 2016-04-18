#include "game.h"

Display::Display(): user_name("Unknown"), level("Terrestrial"), steps (0), energy (15)
{
}

void Display::SetName(){
	printw("Please Enter Your Name:");
	getstr(user_name);
}

string Display:: GetName(){
  return user_name;
}

string Display:: GetLevel() {
  return level;
}

int Display:: GetEnergy() {
  return energy;
}

int Display:: GetSteps(){
  return steps;
}

