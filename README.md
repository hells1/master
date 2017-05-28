# masterimport java.awt.*;
import java.awt.event.*;

import javax.swing.*;
 
public class TicTacLayout extends JFrame {
    private JLabel label;
    private JButton button;
    public TicTacLayout(String name) {
         super(name);
    }
    

    public void addComponentsToPane(final Container pane) {
        JPanel buttonPanel = new JPanel();
        buttonPanel.setLayout(new GridLayout(3,3));
        
        JButton buttonName = new JButton("*");
        ActionListener listener = null;
		buttonName.addActionListener(listener);

        //Add buttons to experiment with Grid Layout
        JPanel buttonPanel1 = new JPanel();
 		buttonName.addActionListener(listener);
 		label.setText("X");
        JPanel buttonPanel2 = new JPanel();
		buttonName.addActionListener(listener);
		label.setText("O");
		JPanel buttonPanel3 = new JPanel();
 		buttonName.addActionListener(listener);
 		label.setText("X");
        JPanel buttonPanel4 = new JPanel();
		buttonName.addActionListener(listener);
		label.setText("O");
		JPanel buttonPanel5 = new JPanel();
 		buttonName.addActionListener(listener);
 		label.setText("X");
        JPanel buttonPanel6 = new JPanel();
		buttonName.addActionListener(listener);
		label.setText("O");
		JPanel buttonPanel7 = new JPanel();
 		buttonName.addActionListener(listener);
 		label.setText("X");
        JPanel buttonPanel8 = new JPanel();
		buttonName.addActionListener(listener);
		label.setText("O");
		JPanel buttonPanel9 = new JPanel();
 		buttonName.addActionListener(listener);
 		label.setText("X");
        pane.add(buttonPanel);
        
    }
    
    /**
     * Create the GUI and show it.  For thread safety,
     * this method is invoked from the
     * event dispatch thread.
     */
    private static void createAndShowGUI() {
        //Create and set up the window.
        TicTacLayout frame = new TicTacLayout("TicTac Layout");
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        //Set up the content pane.
        frame.addComponentsToPane(frame.getContentPane());
        //Display the window.
        frame.pack();
        frame.setVisible(true);
    }
     
    public static void main(String[] args) {
        /* Use an appropriate Look and Feel */
        try {
            //UIManager.setLookAndFeel("com.sun.java.swing.plaf.windows.WindowsLookAndFeel");
            UIManager.setLookAndFeel("javax.swing.plaf.metal.MetalLookAndFeel");
        } catch (UnsupportedLookAndFeelException ex) {
            ex.printStackTrace();
        } catch (IllegalAccessException ex) {
            ex.printStackTrace();
        } catch (InstantiationException ex) {
            ex.printStackTrace();
        } catch (ClassNotFoundException ex) {
            ex.printStackTrace();
        }
        /* Turn off metal's use of bold fonts */
        UIManager.put("swing.boldMetal", Boolean.FALSE);
         
        //Schedule a job for the event dispatch thread:
        //creating and showing this application's GUI.
        javax.swing.SwingUtilities.invokeLater(new Runnable() {
            public void run() {
                createAndShowGUI();
            }
        });
    }
}
