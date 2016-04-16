#include <game.h>

Display::Display(): user_name("Unknown"), level("Terrestrial"), stpes (0), energy (15)
{
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

void display_init()
{
	initscr();			/* Start curses */
	raw();
	echo();
}

void display_close()
{
	endwin();			/* End curses   */
	exit(0);			/* Make clean exit */
}

void clearDisplay(int num){
	if(num==0)
	clear();
	else{
	clear();
	std::ifstream banner ("banner.txt"); 
	displaytext(banner);}
	refresh();
}

void Display::intro_display()
{
  printw("Hello: ");
  printw("%s", user_name);
  printw("         Level:");
  printw("%s", level);
  printw("         Energy:");
  printw("%d", energy);
  printw("         Steps:");
  printw("%d", steps);
}
