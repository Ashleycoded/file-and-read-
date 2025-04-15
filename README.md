# file-and-read-
def modify_file(input_filename, output_filename):
    try:
        with open(input_filename, 'r') as infile, open(output_filename, 'w') as outfile:
            for line in infile:
                modified_line = line.upper()  # Example modification
                outfile.write(modified_line)
        print(f"Modified content written to {output_filename}")
    except FileNotFoundError:
        print(f"Error: File '{input_filename}' not found.")
    except Exception as e:
        print(f"An error occurred: {e}")

# Example usage:
input_file = input("Enter the name of the input file: ")
output_file = input("Enter the name for the output file: ")
modify_file(input_file, output_file)
