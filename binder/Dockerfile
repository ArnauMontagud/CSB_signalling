# What Binder builds for this practical.
#
# Same approach as the official CoLoMoTo Binder: pin a dated CoLoMoTo image
# instead of letting conda resolve the environment at build time. The image is
# already built, so Binder pulls it instead of solving 311 packages, and the
# versions cannot drift from one launch to the next.
#
# 2025-03-01 is the image verified to work with this notebook. Do not move to a
# 2026 image without running the notebook end to end first: in the 2026 GINsim
# builds the bioLQM tool registry comes back empty and biolqm.fixpoints
# disappears.
#
# Note: because this binder/ directory exists, repo2docker ignores the
# environment.yml at the root of the repository. That file stays for people
# installing locally with conda.

FROM colomoto/colomoto-docker:2025-03-01

USER root
COPY . /notebook/
RUN chown -R user:user /notebook
USER user
